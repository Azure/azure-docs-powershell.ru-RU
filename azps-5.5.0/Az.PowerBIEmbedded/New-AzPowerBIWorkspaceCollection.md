---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 557b1b7c5c2a91ec5e77729e70d2aa58f696d212
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236209"
---
# <span data-ttu-id="9fb82-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9fb82-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="9fb82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fb82-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb82-103">Создает коллекцию рабочих области Power BI.</span><span class="sxs-lookup"><span data-stu-id="9fb82-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="9fb82-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9fb82-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fb82-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fb82-105">DESCRIPTION</span></span>
<span data-ttu-id="9fb82-106">Командлет **New-AzPowerBIWorkspaceCollection** создает коллекцию рабочей области Power BI для подписки На Azure в указанной группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="9fb82-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="9fb82-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9fb82-107">EXAMPLES</span></span>

### <span data-ttu-id="9fb82-108">Пример 1. Создание коллекции рабочих области</span><span class="sxs-lookup"><span data-stu-id="9fb82-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="9fb82-109">Эта команда создает коллекцию рабочей области с именем WCN11 в указанной группе ресурсов в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="9fb82-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="9fb82-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fb82-110">PARAMETERS</span></span>

### <span data-ttu-id="9fb82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb82-111">-DefaultProfile</span></span>
<span data-ttu-id="9fb82-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9fb82-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fb82-113">-Location</span><span class="sxs-lookup"><span data-stu-id="9fb82-113">-Location</span></span>
<span data-ttu-id="9fb82-114">Определяет расположение Azure, в котором этот cmdlet создает коллекцию рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9fb82-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="9fb82-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fb82-115">-ResourceGroupName</span></span>
<span data-ttu-id="9fb82-116">Имя группы ресурсов, в которой этот cmdlet создает коллекцию рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9fb82-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="9fb82-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="9fb82-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="9fb82-118">Имя коллекции рабочей области Power BI.</span><span class="sxs-lookup"><span data-stu-id="9fb82-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="9fb82-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fb82-119">-Confirm</span></span>
<span data-ttu-id="9fb82-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9fb82-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fb82-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fb82-121">-WhatIf</span></span>
<span data-ttu-id="9fb82-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fb82-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fb82-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9fb82-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fb82-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb82-124">CommonParameters</span></span>
<span data-ttu-id="9fb82-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fb82-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb82-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fb82-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb82-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fb82-127">INPUTS</span></span>

### <span data-ttu-id="9fb82-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9fb82-128">System.String</span></span>

## <span data-ttu-id="9fb82-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9fb82-129">OUTPUTS</span></span>

### <span data-ttu-id="9fb82-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9fb82-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="9fb82-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9fb82-131">NOTES</span></span>

## <span data-ttu-id="9fb82-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fb82-132">RELATED LINKS</span></span>

[<span data-ttu-id="9fb82-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9fb82-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="9fb82-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9fb82-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


