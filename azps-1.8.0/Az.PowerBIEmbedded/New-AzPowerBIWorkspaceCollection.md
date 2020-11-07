---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: c16632f621af0dfe3f6b6a1b53148eef2c480e8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729806"
---
# <span data-ttu-id="7bfbd-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="7bfbd-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="7bfbd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7bfbd-102">SYNOPSIS</span></span>
<span data-ttu-id="7bfbd-103">Создает набор рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="7bfbd-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="7bfbd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7bfbd-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bfbd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bfbd-105">DESCRIPTION</span></span>
<span data-ttu-id="7bfbd-106">Командлет **New-AzPowerBIWorkspaceCollection** создает набор рабочих областей Power BI для подписки Azure в указанной группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="7bfbd-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="7bfbd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7bfbd-107">EXAMPLES</span></span>

### <span data-ttu-id="7bfbd-108">Пример 1: создание коллекции рабочих областей</span><span class="sxs-lookup"><span data-stu-id="7bfbd-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="7bfbd-109">Эта команда создает коллекцию рабочих областей с именем WCN11 в указанной группе ресурсов в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="7bfbd-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="7bfbd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7bfbd-110">PARAMETERS</span></span>

### <span data-ttu-id="7bfbd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bfbd-111">-DefaultProfile</span></span>
<span data-ttu-id="7bfbd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7bfbd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bfbd-113">-Location</span><span class="sxs-lookup"><span data-stu-id="7bfbd-113">-Location</span></span>
<span data-ttu-id="7bfbd-114">Указывает расположение Azure, в котором этот командлет создает коллекцию рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="7bfbd-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bfbd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bfbd-115">-ResourceGroupName</span></span>
<span data-ttu-id="7bfbd-116">Указывает имя группы ресурсов, в которой этот командлет создает коллекцию рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="7bfbd-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="7bfbd-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="7bfbd-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="7bfbd-118">Задает имя коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="7bfbd-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="7bfbd-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bfbd-119">-Confirm</span></span>
<span data-ttu-id="7bfbd-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7bfbd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bfbd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bfbd-121">-WhatIf</span></span>
<span data-ttu-id="7bfbd-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7bfbd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bfbd-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7bfbd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bfbd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bfbd-124">CommonParameters</span></span>
<span data-ttu-id="7bfbd-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7bfbd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bfbd-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bfbd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bfbd-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7bfbd-127">INPUTS</span></span>

### <span data-ttu-id="7bfbd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7bfbd-128">System.String</span></span>

## <span data-ttu-id="7bfbd-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bfbd-129">OUTPUTS</span></span>

### <span data-ttu-id="7bfbd-130">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="7bfbd-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="7bfbd-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7bfbd-131">NOTES</span></span>

## <span data-ttu-id="7bfbd-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7bfbd-132">RELATED LINKS</span></span>

[<span data-ttu-id="7bfbd-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="7bfbd-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="7bfbd-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="7bfbd-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


