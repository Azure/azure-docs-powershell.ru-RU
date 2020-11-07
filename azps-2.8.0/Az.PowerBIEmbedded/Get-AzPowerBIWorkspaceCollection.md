---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 19b1d1b0da719167d53739a8c92a97121656aa9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904517"
---
# <span data-ttu-id="fa8bc-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="fa8bc-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="fa8bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="fa8bc-103">Получение коллекций рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="fa8bc-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="fa8bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa8bc-104">SYNTAX</span></span>

### <span data-ttu-id="fa8bc-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa8bc-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa8bc-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa8bc-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa8bc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa8bc-107">DESCRIPTION</span></span>
<span data-ttu-id="fa8bc-108">Командлет **Get-AzPowerBIWorkspaceCollection** получает наборы рабочих областей Power BI в подписке и группе ресурсов Azure, а также по имени коллекции.</span><span class="sxs-lookup"><span data-stu-id="fa8bc-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="fa8bc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa8bc-109">EXAMPLES</span></span>

### <span data-ttu-id="fa8bc-110">Пример 1: получение всех коллекций рабочих областей в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="fa8bc-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="fa8bc-111">Эта команда возвращает коллекции рабочих областей, которые принадлежат группе ресурсов с именем ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="fa8bc-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="fa8bc-112">Пример 2: получение коллекции рабочих областей с использованием ее имени</span><span class="sxs-lookup"><span data-stu-id="fa8bc-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="fa8bc-113">Эта команда получает набор рабочих областей с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fa8bc-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="fa8bc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa8bc-114">PARAMETERS</span></span>

### <span data-ttu-id="fa8bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa8bc-115">-DefaultProfile</span></span>
<span data-ttu-id="fa8bc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fa8bc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa8bc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa8bc-117">-ResourceGroupName</span></span>
<span data-ttu-id="fa8bc-118">Указывает имя группы ресурсов, из которой этот командлет получает коллекции рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="fa8bc-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="fa8bc-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="fa8bc-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="fa8bc-120">Указывает имя коллекции рабочих областей Power BI, которую этот командлет получает.</span><span class="sxs-lookup"><span data-stu-id="fa8bc-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fa8bc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa8bc-121">CommonParameters</span></span>
<span data-ttu-id="fa8bc-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa8bc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa8bc-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa8bc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa8bc-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa8bc-124">INPUTS</span></span>

### <span data-ttu-id="fa8bc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fa8bc-125">System.String</span></span>

## <span data-ttu-id="fa8bc-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa8bc-126">OUTPUTS</span></span>

### <span data-ttu-id="fa8bc-127">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="fa8bc-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="fa8bc-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa8bc-128">NOTES</span></span>

## <span data-ttu-id="fa8bc-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa8bc-129">RELATED LINKS</span></span>

[<span data-ttu-id="fa8bc-130">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="fa8bc-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="fa8bc-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="fa8bc-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


