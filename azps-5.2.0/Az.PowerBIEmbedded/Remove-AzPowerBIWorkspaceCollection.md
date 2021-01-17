---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: c8e6f54b5bd4deeb4ef24559298306880740c6d3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403943"
---
# <span data-ttu-id="6fd8f-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6fd8f-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="6fd8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fd8f-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd8f-103">Удаляет коллекцию рабочей области Power BI.</span><span class="sxs-lookup"><span data-stu-id="6fd8f-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="6fd8f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6fd8f-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fd8f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fd8f-105">DESCRIPTION</span></span>
<span data-ttu-id="6fd8f-106">Командлет **Remove-AzPowerBIWorkspaceCollection** удаляет коллекцию рабочей области Power BI из вашей подписки и группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd8f-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="6fd8f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6fd8f-107">EXAMPLES</span></span>

### <span data-ttu-id="6fd8f-108">Пример 1. Удаление коллекции рабочей области</span><span class="sxs-lookup"><span data-stu-id="6fd8f-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="6fd8f-109">Эта команда удаляет коллекцию рабочей области с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6fd8f-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="6fd8f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fd8f-110">PARAMETERS</span></span>

### <span data-ttu-id="6fd8f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd8f-111">-DefaultProfile</span></span>
<span data-ttu-id="6fd8f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6fd8f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fd8f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd8f-113">-ResourceGroupName</span></span>
<span data-ttu-id="6fd8f-114">Имя группы ресурсов, из которой этот cmdlet удаляет коллекцию рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6fd8f-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="6fd8f-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="6fd8f-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="6fd8f-116">Имя коллекции рабочей области Power BI, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fd8f-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6fd8f-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fd8f-117">-Confirm</span></span>
<span data-ttu-id="6fd8f-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fd8f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fd8f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd8f-119">-WhatIf</span></span>
<span data-ttu-id="6fd8f-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fd8f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fd8f-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6fd8f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fd8f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd8f-122">CommonParameters</span></span>
<span data-ttu-id="6fd8f-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd8f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd8f-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd8f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd8f-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fd8f-125">INPUTS</span></span>

### <span data-ttu-id="6fd8f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6fd8f-126">System.String</span></span>

## <span data-ttu-id="6fd8f-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6fd8f-127">OUTPUTS</span></span>

### <span data-ttu-id="6fd8f-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="6fd8f-128">System.Void</span></span>

## <span data-ttu-id="6fd8f-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6fd8f-129">NOTES</span></span>

## <span data-ttu-id="6fd8f-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fd8f-130">RELATED LINKS</span></span>

[<span data-ttu-id="6fd8f-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6fd8f-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="6fd8f-132">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6fd8f-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


