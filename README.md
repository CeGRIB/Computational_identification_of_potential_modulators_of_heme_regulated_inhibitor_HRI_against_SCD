# Computational_identification_of_potential_modulators_of_heme_regulated_inhibitor_HRI_against_SCD
Computational identification of potential modulators of heme-regulated inhibitor (HRI) for pharmacological intervention against sickle cell disease

```
## Usage
```

## import library

```
library(ggplot2)
library(ggrepel)
library(readxl)
```

## read data
```
Cannabiscitrin <- read_excel("Can_P_RMSF.xlsx")
Epigallocatechin <- read_excel('Epi_P_RMSF.xlsx')
Kaempferol <- read_excel('Kaemp_P_RMSF.xlsx')
Myricetin <- read_excel('Myri_P_RMSF.xlsx')
Tiliroside <- read_excel('Til_P_RMSF.xlsx')
```

## Create a .pdf out
```
pdf(file = 'Supplementary.pdf',useDingbats = F, paper = 'a4r', width = 40, height = 40)
``

### make a plot for cannabiscitrin complex
```
ggplot(data = Cannabiscitrin, aes(label = ResName, y= Backbone, x=CA))+
  geom_line(color='darkorchid', lwd=0.4)+
  geom_point(data = subset(Cannabiscitrin, LigandContact == 'Yes'), size=0.5, color='black')+
  geom_text_repel(data = subset(Cannabiscitrin, LigandContact == 'Yes'), aes(label=ResName), size=3, color='maroon2')+
  ggtitle("Amino acid residues forming contact with cannabiscitrin") +
  xlab("C alpha") + ylab("Backbone") +
  theme_bw()+
  theme(axis.text.x = element_text(color="Black"),
        axis.text.y = element_text(color="Black"),
        plot.title = element_text(color="black", size=14, face="bold.italic"),
        axis.title.x = element_text(color="black", size=12, face="bold"),
        axis.title.y = element_text(color="black", size=12, face="bold"))+
  scale_x_continuous(breaks = seq(5, 30, by = 5))+
  scale_y_continuous(breaks = seq(5, 30, by = 5))+
  theme(panel.grid.major = element_blank(), panel.grid.minor = element_blank())
```


### make a plot epigallocatechin gallate complex
```
ggplot(data = Epigallocatechin, aes(label = ResName, y= Backbone, x=CA))+
  geom_line(color='blue', lwd=0.4)+
  geom_point(data = subset(Epigallocatechin, LigandContact == 'Yes'), size=0.5, color='black')+
  geom_text_repel(data = subset(Epigallocatechin, LigandContact == 'Yes'), aes(label=ResName), size=3, color='maroon2')+
  ggtitle("Amino acid residues forming contact with epigallocatechin gallate") +
  xlab("C alpha") + ylab("Backbone") +
  theme_bw()+
  theme(axis.text.x = element_text(color="Black"),
        axis.text.y = element_text(color="Black"),
        plot.title = element_text(color="black", size=14, face="bold.italic"),
        axis.title.x = element_text(color="black", size=12, face="bold"),
        axis.title.y = element_text(color="black", size=12, face="bold"))+
  scale_x_continuous(breaks = seq(1, 6, by = 1))+
  scale_y_continuous(breaks = seq(1, 6, by = 1))+
  theme(panel.grid.major = element_blank(), panel.grid.minor = element_blank())
```


### make a plot for Kaempferol-3-(2G-glucosylrutinoside) complex
```
ggplot(data = Kaempferol, aes(label = ResName, y= Backbone, x=CA))+
  geom_line(color='red', lwd=0.4)+
  geom_point(data = subset(Kaempferol, LigandContact == 'Yes'), size=0.5, color='black')+
  geom_text_repel(data = subset(Kaempferol, LigandContact == 'Yes'), aes(label=ResName), size=3, color='maroon2')+
  ggtitle("Amino acid residues forming contact with Kaempferol-3-(2G-glucosylrutinoside)" +
  xlab("C alpha") + ylab("Backbone") +
  theme_bw()+
  theme(axis.text.x = element_text(color="Black"),
        axis.text.y = element_text(color="Black"),
        plot.title = element_text(color="black", size=14, face="bold.italic"),
        axis.title.x = element_text(color="black", size=12, face="bold"),
        axis.title.y = element_text(color="black", size=12, face="bold"))+
  scale_x_continuous(breaks = seq(1, 10, by = 1))+
  scale_y_continuous(breaks = seq(1, 10, by = 1))+
  theme(panel.grid.major = element_blank(), panel.grid.minor = element_blank())
```


### make a plot for myricetin complex
```
ggplot(data = Myricetin, aes(label = ResName, y= Backbone, x=CA))+
  geom_line(color='springgreen3', lwd=0.4)+
  geom_point(data = subset(Myricetin, LigandContact == 'Yes'), size=0.5, color='black')+
  geom_text_repel(data = subset(Myricetin, LigandContact == 'Yes'), aes(label=ResName), size=3, color='maroon2')+
  ggtitle("Amino acid residues forming contact with Myricetin") +
  xlab("C alpha") + ylab("Backbone") +
  theme_bw()+
  theme(axis.text.x = element_text(color="Black"),
        axis.text.y = element_text(color="Black"),
        plot.title = element_text(color="black", size=14, face="bold.italic"),
        axis.title.x = element_text(color="black", size=12, face="bold"),
        axis.title.y = element_text(color="black", size=12, face="bold"))+
  scale_x_continuous(breaks = seq(0.5, 2, by = 0.5))+
  scale_y_continuous(breaks = seq(0.5, 2, by = 0.5))+
  theme(panel.grid.major = element_blank(), panel.grid.minor = element_blank())
```


### make a plot for tiliroside complex
```
ggplot(data = Tiliroside, aes(label = ResName, y= Backbone, x=CA))+
  geom_line(color='orange2', lwd=0.4)+
  geom_point(data = subset(Tiliroside, LigandContact == 'Yes'), size=0.5, color='black')+
  geom_text_repel(data = subset(Tiliroside, LigandContact == 'Yes'), aes(label=ResName), size=3, color='maroon2')+
  ggtitle("Amino acid residues forming contact with tiliroside") +
  xlab("C alpha") + ylab("Backbone") +
  theme_bw()+
  theme(axis.text.x = element_text(color="Black"),
        axis.text.y = element_text(color="Black"),
        plot.title = element_text(color="black", size=14, face="bold.italic"),
        axis.title.x = element_text(color="black", size=12, face="bold"),
        axis.title.y = element_text(color="black", size=12, face="bold"))+
  scale_x_continuous(breaks = seq(2, 10, by = 2))+
  scale_y_continuous(breaks = seq(2, 10, by = 2))+
  theme(panel.grid.major = element_blank(), panel.grid.minor = element_blank())
```


```
dev.off()
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
