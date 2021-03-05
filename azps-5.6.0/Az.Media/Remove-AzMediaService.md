---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 5b27574dc6ea60472a16c0b647027ceba17a87b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006584"
---
# <span data-ttu-id="0afd0-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0afd0-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="0afd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0afd0-102">SYNOPSIS</span></span>
<span data-ttu-id="0afd0-103">Удаляет службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0afd0-103">Removes a media service.</span></span>

## <span data-ttu-id="0afd0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0afd0-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0afd0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0afd0-105">DESCRIPTION</span></span>
<span data-ttu-id="0afd0-106">Для **удаления службы** мультимедиа будет удаляема служба мультимедиа с ее начертаемой службой.</span><span class="sxs-lookup"><span data-stu-id="0afd0-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="0afd0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0afd0-107">EXAMPLES</span></span>

### <span data-ttu-id="0afd0-108">Пример 1. Удаление службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0afd0-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="0afd0-109">Эта команда удаляет службу мультимедиа с именем MediaService0011 в группе ресурсов ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="0afd0-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="0afd0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0afd0-110">PARAMETERS</span></span>

### <span data-ttu-id="0afd0-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0afd0-111">-AccountName</span></span>
<span data-ttu-id="0afd0-112">Указывает имя службы мультимедиа, которую этот cmdlet удаляет.</span><span class="sxs-lookup"><span data-stu-id="0afd0-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0afd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afd0-113">-DefaultProfile</span></span>
<span data-ttu-id="0afd0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0afd0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0afd0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0afd0-115">-Force</span></span>
<span data-ttu-id="0afd0-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0afd0-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afd0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0afd0-117">-ResourceGroupName</span></span>
<span data-ttu-id="0afd0-118">Имя группы ресурсов, которая содержит службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0afd0-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="0afd0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0afd0-119">-Confirm</span></span>
<span data-ttu-id="0afd0-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0afd0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0afd0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0afd0-121">-WhatIf</span></span>
<span data-ttu-id="0afd0-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0afd0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0afd0-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0afd0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0afd0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afd0-124">CommonParameters</span></span>
<span data-ttu-id="0afd0-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0afd0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afd0-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0afd0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afd0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0afd0-127">INPUTS</span></span>

### <span data-ttu-id="0afd0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0afd0-128">System.String</span></span>

## <span data-ttu-id="0afd0-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0afd0-129">OUTPUTS</span></span>

### <span data-ttu-id="0afd0-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0afd0-130">System.Boolean</span></span>

## <span data-ttu-id="0afd0-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0afd0-131">NOTES</span></span>

## <span data-ttu-id="0afd0-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0afd0-132">RELATED LINKS</span></span>

[<span data-ttu-id="0afd0-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0afd0-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="0afd0-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0afd0-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="0afd0-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0afd0-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


