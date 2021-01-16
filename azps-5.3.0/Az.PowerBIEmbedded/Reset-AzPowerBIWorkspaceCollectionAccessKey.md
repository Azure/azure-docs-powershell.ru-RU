---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: d9e30c81eb0e2422b91be79bcfc7c732291c30cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506814"
---
# <span data-ttu-id="c2abb-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="c2abb-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="c2abb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2abb-102">SYNOPSIS</span></span>
<span data-ttu-id="c2abb-103">Сбрасывает указанный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="c2abb-103">Resets the specified access key.</span></span>

## <span data-ttu-id="c2abb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2abb-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2abb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2abb-105">DESCRIPTION</span></span>
<span data-ttu-id="c2abb-106">Командлет **Reset-AzPowerBIWorkspaceCollectionAccessKey** сбрасывает указанный ключ доступа в коллекции рабочей области Power BI.</span><span class="sxs-lookup"><span data-stu-id="c2abb-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="c2abb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2abb-107">EXAMPLES</span></span>

### <span data-ttu-id="c2abb-108">Пример 1. Сброс первичного ключа доступа</span><span class="sxs-lookup"><span data-stu-id="c2abb-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="c2abb-109">Эта команда сбрасывает первичный ключ доступа для коллекции рабочей области "WCN11" в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2abb-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="c2abb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2abb-110">PARAMETERS</span></span>

### <span data-ttu-id="c2abb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2abb-111">-DefaultProfile</span></span>
<span data-ttu-id="c2abb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c2abb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2abb-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="c2abb-113">-Key1</span></span>
<span data-ttu-id="c2abb-114">Указывает на то, что этот cmdlet сбрасывает первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="c2abb-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="c2abb-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="c2abb-115">-Key2</span></span>
<span data-ttu-id="c2abb-116">Указывает на то, что этот cmdlet сбрасывает клавишу дополнительного доступа.</span><span class="sxs-lookup"><span data-stu-id="c2abb-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="c2abb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2abb-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2abb-118">Определяет имя группы ресурсов коллекции.</span><span class="sxs-lookup"><span data-stu-id="c2abb-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="c2abb-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="c2abb-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="c2abb-120">Определяет имя коллекции рабочей области Power BI, для которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2abb-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c2abb-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2abb-121">-Confirm</span></span>
<span data-ttu-id="c2abb-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c2abb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2abb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2abb-123">-WhatIf</span></span>
<span data-ttu-id="c2abb-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2abb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2abb-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c2abb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2abb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2abb-126">CommonParameters</span></span>
<span data-ttu-id="c2abb-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2abb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2abb-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2abb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2abb-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2abb-129">INPUTS</span></span>

### <span data-ttu-id="c2abb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c2abb-130">System.String</span></span>

## <span data-ttu-id="c2abb-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2abb-131">OUTPUTS</span></span>

### <span data-ttu-id="c2abb-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="c2abb-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="c2abb-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2abb-133">NOTES</span></span>

## <span data-ttu-id="c2abb-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2abb-134">RELATED LINKS</span></span>

[<span data-ttu-id="c2abb-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="c2abb-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


