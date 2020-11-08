---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F41E3B17-A33C-4FBF-B532-2E86F1AAE2B8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4bc3e4245e3d223d95c3ec5d793a53d5d3bfbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076259"
---
# <span data-ttu-id="e17f2-101">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="e17f2-101">Import-AzureStorSimpleLegacyApplianceConfig</span></span>

## <span data-ttu-id="e17f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e17f2-102">SYNOPSIS</span></span>
<span data-ttu-id="e17f2-103">Импорт файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e17f2-103">Imports a configuration file.</span></span>

## <span data-ttu-id="e17f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e17f2-104">SYNTAX</span></span>

```
Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath <String> -TargetDeviceName <String>
 -ConfigDecryptionKey <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e17f2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e17f2-105">DESCRIPTION</span></span>
<span data-ttu-id="e17f2-106">Командлет **Import-AzureStorSimpleLegacyApplianceConfig** импортирует файл конфигурации из устаревшего устройства.</span><span class="sxs-lookup"><span data-stu-id="e17f2-106">The **Import-AzureStorSimpleLegacyApplianceConfig** cmdlet imports the configuration file from the legacy appliance.</span></span>
<span data-ttu-id="e17f2-107">Этот файл включает сведения о контейнерах томов, политиках резервного копирования и учетной записи хранения для службы Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="e17f2-107">That file contains information about volume containers, backup policies, and storage account credentials for the Azure StorSimple service.</span></span>
<span data-ttu-id="e17f2-108">Этот командлет возвращает метаданные конфигурации для старого устройства.</span><span class="sxs-lookup"><span data-stu-id="e17f2-108">This cmdlet returns the legacy appliance configuration metadata.</span></span>

## <span data-ttu-id="e17f2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e17f2-109">EXAMPLES</span></span>

### <span data-ttu-id="e17f2-110">Пример 1: импорт файла конфигурации</span><span class="sxs-lookup"><span data-stu-id="e17f2-110">Example 1: Import a configuration file</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath "C:\MigrationData\LegacyStorSimpleConfig.sse" -TargetDeviceName "8100-123456789" -ConfigDecryptionKey "fWs793hHVhR90NKdDYTeNq"
LegacyConfigId      : e2d5c9b1-b528-4c21-b8ae-533feefc8a41
ImportedOn          : 4/8/2015 7:23:04 PM
ConfigFile          : D:\configs\StorSimpleConfig_27_Mar_15_12_19.xml.sse
TargetApplianceName : Arunkm-N4
Details             : Available Cloud Configuration(s) for migration : 
                          Cloud Configuration(s) 1    : TC8Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 2    : fulle_cc4
                          Cloud Configuration(s) 3    : fulle_cc2
                          Cloud Configuration(s) 4    : fulle_cc3
                          Cloud Configuration(s) 5    : TC9Cloud[Stingray18-FP3] 
                          Cloud Configuration(s) 6    : fulle_cc1
                          Cloud Configuration(s) 7    : Container-New[Stingray19-FP6] 
                          Cloud Configuration(s) 8    : TC6Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 9    : TC7Cloud[Stingray18-FP3] 

Result              : Successfully imported config from the legacy appliance! 
Save the legacy config id and cloud configuration(s) for future reference.
```

<span data-ttu-id="e17f2-111">Эта команда импортирует файл конфигурации по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="e17f2-111">This command imports the configuration file at the specified path.</span></span>
<span data-ttu-id="e17f2-112">Команда включает ключ для расшифровки файла.</span><span class="sxs-lookup"><span data-stu-id="e17f2-112">The command includes the key to decrypt the file.</span></span>

## <span data-ttu-id="e17f2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e17f2-113">PARAMETERS</span></span>

### <span data-ttu-id="e17f2-114">-ConfigDecryptionKey</span><span class="sxs-lookup"><span data-stu-id="e17f2-114">-ConfigDecryptionKey</span></span>
<span data-ttu-id="e17f2-115">Задает ключ расшифровки для конфигурации устаревшего устройства.</span><span class="sxs-lookup"><span data-stu-id="e17f2-115">Specifies the decryption key for the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17f2-116">-ConfigFilePath</span><span class="sxs-lookup"><span data-stu-id="e17f2-116">-ConfigFilePath</span></span>
<span data-ttu-id="e17f2-117">Указывает абсолютный путь к файлу конфигурации, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="e17f2-117">Specifies the absolute path of the configuration file to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17f2-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="e17f2-118">-Profile</span></span>
<span data-ttu-id="e17f2-119">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="e17f2-119">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17f2-120">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="e17f2-120">-TargetDeviceName</span></span>
<span data-ttu-id="e17f2-121">Указывает имя оконечного устройства, представленное на портале.</span><span class="sxs-lookup"><span data-stu-id="e17f2-121">Specifies the name of the target device as presented in the portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17f2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e17f2-122">CommonParameters</span></span>
<span data-ttu-id="e17f2-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e17f2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e17f2-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e17f2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e17f2-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e17f2-125">INPUTS</span></span>

### <span data-ttu-id="e17f2-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="e17f2-126">None</span></span>

## <span data-ttu-id="e17f2-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e17f2-127">OUTPUTS</span></span>

### <span data-ttu-id="e17f2-128">LegacyApplianceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e17f2-128">LegacyApplianceConfiguration</span></span>
<span data-ttu-id="e17f2-129">Этот командлет возвращает сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e17f2-129">This cmdlet returns the details of the configuration.</span></span>
<span data-ttu-id="e17f2-130">Объект **LegacyApplianceConfiguration** включает следующие сведения: ИД конфигурации, имена контейнеров томов, элементы управления доступом, политики резервного копирования, параметры пропускной способности, контейнеры томов, учетные данные учетной записи хранения и тома.</span><span class="sxs-lookup"><span data-stu-id="e17f2-130">The **LegacyApplianceConfiguration** object contains the following information: configuration ID, volume container names, access control records, backup policies, bandwidth settings, volume containers, storage account credentials, and volumes.</span></span>

## <span data-ttu-id="e17f2-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e17f2-131">NOTES</span></span>

## <span data-ttu-id="e17f2-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e17f2-132">RELATED LINKS</span></span>

[<span data-ttu-id="e17f2-133">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="e17f2-133">Import-AzureStorSimpleLegacyVolumeContainer</span></span>](./Import-AzureStorSimpleLegacyVolumeContainer.md)


