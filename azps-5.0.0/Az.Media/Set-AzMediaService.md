---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: 5b85e3e64b4a79b33975d9b29d0498ac8ae0ce03
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250085"
---
# <span data-ttu-id="0d871-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0d871-101">Set-AzMediaService</span></span>

## <span data-ttu-id="0d871-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d871-102">SYNOPSIS</span></span>
<span data-ttu-id="0d871-103">Изменяет указанные свойства существующей службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0d871-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="0d871-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d871-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d871-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d871-105">DESCRIPTION</span></span>
<span data-ttu-id="0d871-106">Командлет **Set-AzMediaService** изменяет указанные свойства существующей службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0d871-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="0d871-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d871-107">EXAMPLES</span></span>

### <span data-ttu-id="0d871-108">Пример 1: изменение существующей службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0d871-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="0d871-109">В первой команде создается последовательность тегов и сохраняются эти теги в переменной с именем $Tags.</span><span class="sxs-lookup"><span data-stu-id="0d871-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="0d871-110">Эта вторая команда обновляет службу мультимедиа с именем MediaService001, которая относится к группе ресурсов с именем ResourceGroup123, с тегами, хранящимися в $Tags переменной.</span><span class="sxs-lookup"><span data-stu-id="0d871-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="0d871-111">Команда также использует массив объектов конфигурации хранилища, хранящийся в переменной $StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="0d871-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="0d871-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d871-112">PARAMETERS</span></span>

### <span data-ttu-id="0d871-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="0d871-113">-AccountName</span></span>
<span data-ttu-id="0d871-114">Указывает имя службы мультимедиа, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0d871-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0d871-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d871-115">-DefaultProfile</span></span>
<span data-ttu-id="0d871-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0d871-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d871-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d871-117">-ResourceGroupName</span></span>
<span data-ttu-id="0d871-118">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0d871-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="0d871-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="0d871-119">-StorageAccounts</span></span>
<span data-ttu-id="0d871-120">Указывает массив учетных записей хранения, который этот командлет связывает со службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0d871-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="0d871-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="0d871-121">-Tag</span></span>
<span data-ttu-id="0d871-122">Теги, связанные с учетной записью мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0d871-122">The tags associated with the media account.</span></span>

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

### <span data-ttu-id="0d871-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d871-123">-Confirm</span></span>
<span data-ttu-id="0d871-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d871-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d871-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d871-125">-WhatIf</span></span>
<span data-ttu-id="0d871-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0d871-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d871-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d871-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d871-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d871-128">CommonParameters</span></span>
<span data-ttu-id="0d871-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d871-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d871-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d871-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d871-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d871-131">INPUTS</span></span>

### <span data-ttu-id="0d871-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0d871-132">System.String</span></span>

### <span data-ttu-id="0d871-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0d871-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0d871-134">Microsoft. Azure. Commands. Media. Models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="0d871-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="0d871-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d871-135">OUTPUTS</span></span>

### <span data-ttu-id="0d871-136">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="0d871-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="0d871-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d871-137">NOTES</span></span>

## <span data-ttu-id="0d871-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d871-138">RELATED LINKS</span></span>

[<span data-ttu-id="0d871-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0d871-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="0d871-140">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0d871-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="0d871-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0d871-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


