---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 525c5e2bfd15811e861945a6404e0b88274e2563
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412660"
---
# <span data-ttu-id="26b95-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="26b95-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="26b95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26b95-102">SYNOPSIS</span></span>
<span data-ttu-id="26b95-103">Удаляет службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="26b95-103">Removes a media service.</span></span>

## <span data-ttu-id="26b95-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26b95-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26b95-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26b95-105">DESCRIPTION</span></span>
<span data-ttu-id="26b95-106">Для **удаления службы** мультимедиа будет удаляема служба мультимедиа с ее начертаемой службой.</span><span class="sxs-lookup"><span data-stu-id="26b95-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="26b95-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26b95-107">EXAMPLES</span></span>

### <span data-ttu-id="26b95-108">Пример 1. Удаление службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="26b95-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="26b95-109">Эта команда удаляет службу мультимедиа с именем MediaService0011 в группе ресурсов ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="26b95-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="26b95-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26b95-110">PARAMETERS</span></span>

### <span data-ttu-id="26b95-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="26b95-111">-AccountName</span></span>
<span data-ttu-id="26b95-112">Указывает имя службы мультимедиа, которую этот cmdlet удаляет.</span><span class="sxs-lookup"><span data-stu-id="26b95-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="26b95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b95-113">-DefaultProfile</span></span>
<span data-ttu-id="26b95-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="26b95-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26b95-115">-Force</span><span class="sxs-lookup"><span data-stu-id="26b95-115">-Force</span></span>
<span data-ttu-id="26b95-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="26b95-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26b95-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26b95-117">-ResourceGroupName</span></span>
<span data-ttu-id="26b95-118">Имя группы ресурсов, которая содержит службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="26b95-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="26b95-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26b95-119">-Confirm</span></span>
<span data-ttu-id="26b95-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="26b95-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26b95-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26b95-121">-WhatIf</span></span>
<span data-ttu-id="26b95-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b95-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26b95-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="26b95-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26b95-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b95-124">CommonParameters</span></span>
<span data-ttu-id="26b95-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b95-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b95-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b95-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b95-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26b95-127">INPUTS</span></span>

### <span data-ttu-id="26b95-128">System.String</span><span class="sxs-lookup"><span data-stu-id="26b95-128">System.String</span></span>

## <span data-ttu-id="26b95-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26b95-129">OUTPUTS</span></span>

### <span data-ttu-id="26b95-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26b95-130">System.Boolean</span></span>

## <span data-ttu-id="26b95-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26b95-131">NOTES</span></span>

## <span data-ttu-id="26b95-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26b95-132">RELATED LINKS</span></span>

[<span data-ttu-id="26b95-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="26b95-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="26b95-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="26b95-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="26b95-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="26b95-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


