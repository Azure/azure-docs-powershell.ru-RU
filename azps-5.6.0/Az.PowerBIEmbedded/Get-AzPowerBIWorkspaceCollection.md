---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 99a9d8e4dcf10eaae67516e871c90d78021e6218
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953464"
---
# <span data-ttu-id="fc988-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="fc988-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="fc988-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc988-102">SYNOPSIS</span></span>
<span data-ttu-id="fc988-103">Получает коллекции рабочей области Power BI.</span><span class="sxs-lookup"><span data-stu-id="fc988-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="fc988-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fc988-104">SYNTAX</span></span>

### <span data-ttu-id="fc988-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc988-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc988-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc988-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc988-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc988-107">DESCRIPTION</span></span>
<span data-ttu-id="fc988-108">Командлет **Get-AzPowerBIWorkspaceCollection** получает коллекции рабочей области Power BI в вашей подписке и группе ресурсов Azure или по имени коллекции.</span><span class="sxs-lookup"><span data-stu-id="fc988-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="fc988-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fc988-109">EXAMPLES</span></span>

### <span data-ttu-id="fc988-110">Пример 1. Сбор всех коллекций рабочей области в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="fc988-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="fc988-111">Эта команда возвращает коллекции рабочей области, которые относятся к группе ресурсов с именем ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="fc988-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="fc988-112">Пример 2. Получить коллекцию рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="fc988-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="fc988-113">Эта команда возвращает коллекцию рабочей области "WCN11" в указанную группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc988-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="fc988-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc988-114">PARAMETERS</span></span>

### <span data-ttu-id="fc988-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc988-115">-DefaultProfile</span></span>
<span data-ttu-id="fc988-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fc988-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc988-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc988-117">-ResourceGroupName</span></span>
<span data-ttu-id="fc988-118">Имя группы ресурсов, из которой этот cmdlet получает коллекции рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fc988-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc988-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="fc988-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="fc988-120">Имя коллекции рабочей области Power BI, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc988-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc988-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc988-121">CommonParameters</span></span>
<span data-ttu-id="fc988-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc988-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc988-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc988-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc988-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc988-124">INPUTS</span></span>

### <span data-ttu-id="fc988-125">System.String</span><span class="sxs-lookup"><span data-stu-id="fc988-125">System.String</span></span>

## <span data-ttu-id="fc988-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fc988-126">OUTPUTS</span></span>

### <span data-ttu-id="fc988-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="fc988-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="fc988-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fc988-128">NOTES</span></span>

## <span data-ttu-id="fc988-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc988-129">RELATED LINKS</span></span>

[<span data-ttu-id="fc988-130">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="fc988-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="fc988-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="fc988-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


