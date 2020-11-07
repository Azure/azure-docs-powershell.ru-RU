---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 058a914540cd03bcf523f0300e18299c3cf084ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904506"
---
# <span data-ttu-id="26ab8-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="26ab8-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="26ab8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="26ab8-103">Удаляет набор рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="26ab8-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="26ab8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26ab8-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26ab8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26ab8-105">DESCRIPTION</span></span>
<span data-ttu-id="26ab8-106">Командлет **Remove-AzPowerBIWorkspaceCollection** удаляет набор рабочих областей Power BI из подписки на Azure и группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26ab8-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="26ab8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26ab8-107">EXAMPLES</span></span>

### <span data-ttu-id="26ab8-108">Пример 1: Удаление коллекции рабочих областей</span><span class="sxs-lookup"><span data-stu-id="26ab8-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="26ab8-109">Эта команда удаляет набор рабочих областей с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26ab8-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="26ab8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26ab8-110">PARAMETERS</span></span>

### <span data-ttu-id="26ab8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26ab8-111">-DefaultProfile</span></span>
<span data-ttu-id="26ab8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="26ab8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26ab8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26ab8-113">-ResourceGroupName</span></span>
<span data-ttu-id="26ab8-114">Указывает имя группы ресурсов, из которой этот командлет удаляет коллекцию рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="26ab8-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="26ab8-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="26ab8-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="26ab8-116">Указывает имя коллекции рабочих областей Power BI, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="26ab8-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="26ab8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26ab8-117">-Confirm</span></span>
<span data-ttu-id="26ab8-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26ab8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26ab8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26ab8-119">-WhatIf</span></span>
<span data-ttu-id="26ab8-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26ab8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26ab8-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26ab8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26ab8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26ab8-122">CommonParameters</span></span>
<span data-ttu-id="26ab8-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26ab8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26ab8-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26ab8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26ab8-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26ab8-125">INPUTS</span></span>

### <span data-ttu-id="26ab8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="26ab8-126">System.String</span></span>

## <span data-ttu-id="26ab8-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26ab8-127">OUTPUTS</span></span>

### <span data-ttu-id="26ab8-128">System. void</span><span class="sxs-lookup"><span data-stu-id="26ab8-128">System.Void</span></span>

## <span data-ttu-id="26ab8-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="26ab8-129">NOTES</span></span>

## <span data-ttu-id="26ab8-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26ab8-130">RELATED LINKS</span></span>

[<span data-ttu-id="26ab8-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="26ab8-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="26ab8-132">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="26ab8-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


