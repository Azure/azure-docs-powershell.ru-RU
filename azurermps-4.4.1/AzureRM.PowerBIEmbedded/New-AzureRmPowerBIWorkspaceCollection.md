---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 981daec060f47a88b31454cd8d13711091bedcf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568718"
---
# <span data-ttu-id="2c270-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="2c270-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="2c270-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c270-102">SYNOPSIS</span></span>
<span data-ttu-id="2c270-103">Создает набор рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="2c270-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c270-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c270-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c270-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c270-105">DESCRIPTION</span></span>
<span data-ttu-id="2c270-106">Командлет **New-AzureRmPowerBIWorkspaceCollection** создает набор рабочих областей Power BI для подписки Azure в указанной группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="2c270-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="2c270-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c270-107">EXAMPLES</span></span>

### <span data-ttu-id="2c270-108">Пример 1: создание коллекции рабочих областей</span><span class="sxs-lookup"><span data-stu-id="2c270-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="2c270-109">Эта команда создает коллекцию рабочих областей с именем WCN11 в указанной группе ресурсов в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="2c270-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="2c270-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c270-110">PARAMETERS</span></span>

### <span data-ttu-id="2c270-111">-Location</span><span class="sxs-lookup"><span data-stu-id="2c270-111">-Location</span></span>
<span data-ttu-id="2c270-112">Указывает расположение Azure, в котором этот командлет создает коллекцию рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="2c270-112">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="2c270-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c270-113">-ResourceGroupName</span></span>
<span data-ttu-id="2c270-114">Указывает имя группы ресурсов, в которой этот командлет создает коллекцию рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="2c270-114">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="2c270-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="2c270-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="2c270-116">Задает имя коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="2c270-116">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="2c270-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c270-117">-Confirm</span></span>
<span data-ttu-id="2c270-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c270-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c270-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c270-119">-WhatIf</span></span>
<span data-ttu-id="2c270-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c270-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c270-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c270-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c270-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c270-122">-DefaultProfile</span></span>
<span data-ttu-id="2c270-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c270-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c270-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c270-124">CommonParameters</span></span>
<span data-ttu-id="2c270-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c270-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c270-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c270-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c270-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c270-127">INPUTS</span></span>

## <span data-ttu-id="2c270-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c270-128">OUTPUTS</span></span>

### <span data-ttu-id="2c270-129">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="2c270-129">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="2c270-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c270-130">NOTES</span></span>

## <span data-ttu-id="2c270-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c270-131">RELATED LINKS</span></span>

[<span data-ttu-id="2c270-132">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="2c270-132">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="2c270-133">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="2c270-133">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


