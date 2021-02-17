---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: 5b85e3e64b4a79b33975d9b29d0498ac8ae0ce03
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237425"
---
# <span data-ttu-id="c14d5-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c14d5-101">Set-AzMediaService</span></span>

## <span data-ttu-id="c14d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c14d5-102">SYNOPSIS</span></span>
<span data-ttu-id="c14d5-103">Изменяет указанные свойства существующей службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c14d5-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="c14d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c14d5-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c14d5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c14d5-105">DESCRIPTION</span></span>
<span data-ttu-id="c14d5-106">**Cmdlet Set-AzMediaService** изменяет указанные свойства существующей службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c14d5-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="c14d5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c14d5-107">EXAMPLES</span></span>

### <span data-ttu-id="c14d5-108">Пример 1. Изменение существующей службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c14d5-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="c14d5-109">Первая команда создает ряд тегов и сохраняет их в переменной с $Tags.</span><span class="sxs-lookup"><span data-stu-id="c14d5-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="c14d5-110">Эта вторая команда обновляет службу мультимедиа MediaService001, которая принадлежит к группе ресурсов ResourceGroup123, с тегами, которые хранятся $Tags переменной.</span><span class="sxs-lookup"><span data-stu-id="c14d5-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="c14d5-111">В этой команде также используется массив объектов конфигурации хранилища, которые хранятся $StorageAccounts переменной.</span><span class="sxs-lookup"><span data-stu-id="c14d5-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="c14d5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c14d5-112">PARAMETERS</span></span>

### <span data-ttu-id="c14d5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c14d5-113">-AccountName</span></span>
<span data-ttu-id="c14d5-114">Указывает имя службы мультимедиа, которую изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c14d5-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c14d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14d5-115">-DefaultProfile</span></span>
<span data-ttu-id="c14d5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c14d5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14d5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c14d5-117">-ResourceGroupName</span></span>
<span data-ttu-id="c14d5-118">Имя группы ресурсов, которая содержит службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c14d5-118">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c14d5-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="c14d5-119">-StorageAccounts</span></span>
<span data-ttu-id="c14d5-120">Указывает массив учетных записей хранения, который этот cmdlet связывает со службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c14d5-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c14d5-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="c14d5-121">-Tag</span></span>
<span data-ttu-id="c14d5-122">Теги, связанные с учетной записью мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c14d5-122">The tags associated with the media account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c14d5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c14d5-123">-Confirm</span></span>
<span data-ttu-id="c14d5-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c14d5-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14d5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c14d5-125">-WhatIf</span></span>
<span data-ttu-id="c14d5-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c14d5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c14d5-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c14d5-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14d5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14d5-128">CommonParameters</span></span>
<span data-ttu-id="c14d5-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c14d5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14d5-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c14d5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14d5-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c14d5-131">INPUTS</span></span>

### <span data-ttu-id="c14d5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c14d5-132">System.String</span></span>

### <span data-ttu-id="c14d5-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c14d5-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c14d5-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="c14d5-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="c14d5-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c14d5-135">OUTPUTS</span></span>

### <span data-ttu-id="c14d5-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="c14d5-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="c14d5-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c14d5-137">NOTES</span></span>

## <span data-ttu-id="c14d5-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c14d5-138">RELATED LINKS</span></span>

[<span data-ttu-id="c14d5-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c14d5-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="c14d5-140">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c14d5-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="c14d5-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c14d5-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


