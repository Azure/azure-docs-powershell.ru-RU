---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 557b1b7c5c2a91ec5e77729e70d2aa58f696d212
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065094"
---
# <span data-ttu-id="112d3-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="112d3-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="112d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="112d3-102">SYNOPSIS</span></span>
<span data-ttu-id="112d3-103">Создает набор рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="112d3-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="112d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="112d3-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="112d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="112d3-105">DESCRIPTION</span></span>
<span data-ttu-id="112d3-106">Командлет **New-AzPowerBIWorkspaceCollection** создает набор рабочих областей Power BI для подписки Azure в указанной группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="112d3-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="112d3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="112d3-107">EXAMPLES</span></span>

### <span data-ttu-id="112d3-108">Пример 1: создание коллекции рабочих областей</span><span class="sxs-lookup"><span data-stu-id="112d3-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="112d3-109">Эта команда создает коллекцию рабочих областей с именем WCN11 в указанной группе ресурсов в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="112d3-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="112d3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="112d3-110">PARAMETERS</span></span>

### <span data-ttu-id="112d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="112d3-111">-DefaultProfile</span></span>
<span data-ttu-id="112d3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="112d3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="112d3-113">-Location</span><span class="sxs-lookup"><span data-stu-id="112d3-113">-Location</span></span>
<span data-ttu-id="112d3-114">Указывает расположение Azure, в котором этот командлет создает коллекцию рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="112d3-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="112d3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="112d3-115">-ResourceGroupName</span></span>
<span data-ttu-id="112d3-116">Указывает имя группы ресурсов, в которой этот командлет создает коллекцию рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="112d3-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="112d3-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="112d3-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="112d3-118">Задает имя коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="112d3-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="112d3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="112d3-119">-Confirm</span></span>
<span data-ttu-id="112d3-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="112d3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="112d3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="112d3-121">-WhatIf</span></span>
<span data-ttu-id="112d3-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="112d3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="112d3-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="112d3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="112d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="112d3-124">CommonParameters</span></span>
<span data-ttu-id="112d3-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="112d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="112d3-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="112d3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="112d3-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="112d3-127">INPUTS</span></span>

### <span data-ttu-id="112d3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="112d3-128">System.String</span></span>

## <span data-ttu-id="112d3-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="112d3-129">OUTPUTS</span></span>

### <span data-ttu-id="112d3-130">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="112d3-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="112d3-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="112d3-131">NOTES</span></span>

## <span data-ttu-id="112d3-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="112d3-132">RELATED LINKS</span></span>

[<span data-ttu-id="112d3-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="112d3-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="112d3-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="112d3-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


