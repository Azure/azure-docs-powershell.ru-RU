---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D35C580F-437A-40F9-B6BA-412A1176292A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9821602df196604100de5926a7d9510bdb011bd2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075681"
---
# <span data-ttu-id="e0272-101">Export-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e0272-101">Export-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="e0272-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0272-102">SYNOPSIS</span></span>
<span data-ttu-id="e0272-103">Экспортирует изображение шаблона для одной коллекции RemoteApp Azure в указанную учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="e0272-103">Exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="e0272-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0272-104">SYNTAX</span></span>

```
Export-AzureRemoteAppTemplateImage [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingTemplateImage] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0272-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0272-105">DESCRIPTION</span></span>
<span data-ttu-id="e0272-106">Командлет **Export-AzureRemoteAppTemplateImage** экспортирует образ шаблона для одной коллекции RemoteApp Azure в указанную учетную запись хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e0272-106">The **Export-AzureRemoteAppTemplateImage** cmdlet exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="e0272-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0272-107">EXAMPLES</span></span>

### <span data-ttu-id="e0272-108">Пример 1: Экспорт изображения шаблона в учетную запись хранения Azure</span><span class="sxs-lookup"><span data-stu-id="e0272-108">Example 1: Export a template image to the Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppTemplateImage -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingTemplateImage
```

<span data-ttu-id="e0272-109">Эта команда экспортирует образ шаблона коллекции Contoso в контейнер с именем ContainerName в указанной учетной записи хранения Azure с именем AccountName и ключом AccountKey.</span><span class="sxs-lookup"><span data-stu-id="e0272-109">This command exports the template image of the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="e0272-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0272-110">PARAMETERS</span></span>

### <span data-ttu-id="e0272-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="e0272-111">-CollectionName</span></span>
<span data-ttu-id="e0272-112">Указывает имя исходной коллекции RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="e0272-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0272-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="e0272-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="e0272-114">Указывает имя контейнера в конечной учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e0272-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0272-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e0272-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="e0272-116">Задает ключ учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e0272-116">Specifies the key of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0272-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e0272-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="e0272-118">Указывает имя целевой учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e0272-118">Specifies the name of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0272-119">-OverwriteExistingTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e0272-119">-OverwriteExistingTemplateImage</span></span>
<span data-ttu-id="e0272-120">Указывает на то, что командлет перезапишет существующий образ шаблона.</span><span class="sxs-lookup"><span data-stu-id="e0272-120">Indicates that the cmdlet overwrites the existing template image.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0272-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="e0272-121">-Profile</span></span>
<span data-ttu-id="e0272-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e0272-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0272-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0272-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0272-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0272-124">-Confirm</span></span>
<span data-ttu-id="e0272-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e0272-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0272-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0272-126">-WhatIf</span></span>
<span data-ttu-id="e0272-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e0272-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0272-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e0272-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0272-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0272-129">CommonParameters</span></span>
<span data-ttu-id="e0272-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0272-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0272-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0272-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0272-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0272-132">INPUTS</span></span>

## <span data-ttu-id="e0272-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0272-133">OUTPUTS</span></span>

## <span data-ttu-id="e0272-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0272-134">NOTES</span></span>

## <span data-ttu-id="e0272-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0272-135">RELATED LINKS</span></span>

[<span data-ttu-id="e0272-136">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e0272-136">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="e0272-137">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e0272-137">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="e0272-138">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e0272-138">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="e0272-139">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="e0272-139">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


