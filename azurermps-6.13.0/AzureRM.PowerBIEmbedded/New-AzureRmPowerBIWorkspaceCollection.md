---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7ed4af8c6d5443c3cdc7c8ae395ecc66d0a927e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560779"
---
# <span data-ttu-id="0d36c-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0d36c-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="0d36c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d36c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d36c-103">Создает набор рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="0d36c-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d36c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d36c-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d36c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d36c-105">DESCRIPTION</span></span>
<span data-ttu-id="0d36c-106">Командлет **New-AzureRmPowerBIWorkspaceCollection** создает набор рабочих областей Power BI для подписки Azure в указанной группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="0d36c-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="0d36c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d36c-107">EXAMPLES</span></span>

### <span data-ttu-id="0d36c-108">Пример 1: создание коллекции рабочих областей</span><span class="sxs-lookup"><span data-stu-id="0d36c-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="0d36c-109">Эта команда создает коллекцию рабочих областей с именем WCN11 в указанной группе ресурсов в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="0d36c-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="0d36c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d36c-110">PARAMETERS</span></span>

### <span data-ttu-id="0d36c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d36c-111">-DefaultProfile</span></span>
<span data-ttu-id="0d36c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0d36c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d36c-113">-Location</span><span class="sxs-lookup"><span data-stu-id="0d36c-113">-Location</span></span>
<span data-ttu-id="0d36c-114">Указывает расположение Azure, в котором этот командлет создает коллекцию рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="0d36c-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="0d36c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d36c-115">-ResourceGroupName</span></span>
<span data-ttu-id="0d36c-116">Указывает имя группы ресурсов, в которой этот командлет создает коллекцию рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="0d36c-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="0d36c-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0d36c-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="0d36c-118">Задает имя коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="0d36c-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="0d36c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d36c-119">-Confirm</span></span>
<span data-ttu-id="0d36c-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d36c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d36c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d36c-121">-WhatIf</span></span>
<span data-ttu-id="0d36c-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0d36c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d36c-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d36c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d36c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d36c-124">CommonParameters</span></span>
<span data-ttu-id="0d36c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d36c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d36c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d36c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d36c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d36c-127">INPUTS</span></span>

### <span data-ttu-id="0d36c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0d36c-128">System.String</span></span>

## <span data-ttu-id="0d36c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d36c-129">OUTPUTS</span></span>

### <span data-ttu-id="0d36c-130">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0d36c-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="0d36c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d36c-131">NOTES</span></span>

## <span data-ttu-id="0d36c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d36c-132">RELATED LINKS</span></span>

[<span data-ttu-id="0d36c-133">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0d36c-133">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="0d36c-134">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0d36c-134">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


