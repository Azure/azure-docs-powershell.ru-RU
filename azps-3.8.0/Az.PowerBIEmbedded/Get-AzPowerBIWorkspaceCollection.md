---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: d3be067690b755014fe02840d355fc36e0d6aa20
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065135"
---
# <span data-ttu-id="06c21-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="06c21-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="06c21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06c21-102">SYNOPSIS</span></span>
<span data-ttu-id="06c21-103">Получение коллекций рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="06c21-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="06c21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06c21-104">SYNTAX</span></span>

### <span data-ttu-id="06c21-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="06c21-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06c21-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="06c21-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06c21-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06c21-107">DESCRIPTION</span></span>
<span data-ttu-id="06c21-108">Командлет **Get-AzPowerBIWorkspaceCollection** получает наборы рабочих областей Power BI в подписке и группе ресурсов Azure, а также по имени коллекции.</span><span class="sxs-lookup"><span data-stu-id="06c21-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="06c21-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06c21-109">EXAMPLES</span></span>

### <span data-ttu-id="06c21-110">Пример 1: получение всех коллекций рабочих областей в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="06c21-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="06c21-111">Эта команда возвращает коллекции рабочих областей, которые принадлежат группе ресурсов с именем ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="06c21-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="06c21-112">Пример 2: получение коллекции рабочих областей с использованием ее имени</span><span class="sxs-lookup"><span data-stu-id="06c21-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="06c21-113">Эта команда получает набор рабочих областей с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06c21-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="06c21-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06c21-114">PARAMETERS</span></span>

### <span data-ttu-id="06c21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c21-115">-DefaultProfile</span></span>
<span data-ttu-id="06c21-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="06c21-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06c21-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06c21-117">-ResourceGroupName</span></span>
<span data-ttu-id="06c21-118">Указывает имя группы ресурсов, из которой этот командлет получает коллекции рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="06c21-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="06c21-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="06c21-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="06c21-120">Указывает имя коллекции рабочих областей Power BI, которую этот командлет получает.</span><span class="sxs-lookup"><span data-stu-id="06c21-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="06c21-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c21-121">CommonParameters</span></span>
<span data-ttu-id="06c21-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06c21-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c21-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c21-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c21-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06c21-124">INPUTS</span></span>

### <span data-ttu-id="06c21-125">System. String</span><span class="sxs-lookup"><span data-stu-id="06c21-125">System.String</span></span>

## <span data-ttu-id="06c21-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06c21-126">OUTPUTS</span></span>

### <span data-ttu-id="06c21-127">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="06c21-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="06c21-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="06c21-128">NOTES</span></span>

## <span data-ttu-id="06c21-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06c21-129">RELATED LINKS</span></span>

[<span data-ttu-id="06c21-130">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="06c21-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="06c21-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="06c21-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


