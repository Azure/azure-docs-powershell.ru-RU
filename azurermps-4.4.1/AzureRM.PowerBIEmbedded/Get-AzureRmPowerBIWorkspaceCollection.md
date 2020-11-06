---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 93ca812f726e036d195e83170153f7b2df4a2352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568720"
---
# <span data-ttu-id="07a9e-101">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="07a9e-101">Get-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="07a9e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="07a9e-103">Получение коллекций рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="07a9e-103">Gets Power BI workspace collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07a9e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07a9e-104">SYNTAX</span></span>

### <span data-ttu-id="07a9e-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="07a9e-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07a9e-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="07a9e-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07a9e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07a9e-107">DESCRIPTION</span></span>
<span data-ttu-id="07a9e-108">Командлет **Get-AzureRmPowerBIWorkspaceCollection** получает наборы рабочих областей Power BI в подписке и группе ресурсов Azure, а также по имени коллекции.</span><span class="sxs-lookup"><span data-stu-id="07a9e-108">The **Get-AzureRmPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="07a9e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07a9e-109">EXAMPLES</span></span>

### <span data-ttu-id="07a9e-110">Пример 1: получение всех коллекций рабочих областей в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="07a9e-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="07a9e-111">Эта команда возвращает коллекции рабочих областей, которые принадлежат группе ресурсов с именем ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="07a9e-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="07a9e-112">Пример 2: получение коллекции рабочих областей с использованием ее имени</span><span class="sxs-lookup"><span data-stu-id="07a9e-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="07a9e-113">Эта команда получает набор рабочих областей с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07a9e-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="07a9e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07a9e-114">PARAMETERS</span></span>

### <span data-ttu-id="07a9e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a9e-115">-ResourceGroupName</span></span>
<span data-ttu-id="07a9e-116">Указывает имя группы ресурсов, из которой этот командлет получает коллекции рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="07a9e-116">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="07a9e-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="07a9e-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="07a9e-118">Указывает имя коллекции рабочих областей Power BI, которую этот командлет получает.</span><span class="sxs-lookup"><span data-stu-id="07a9e-118">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="07a9e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a9e-119">-DefaultProfile</span></span>
<span data-ttu-id="07a9e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07a9e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07a9e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a9e-121">CommonParameters</span></span>
<span data-ttu-id="07a9e-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07a9e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a9e-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a9e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a9e-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07a9e-124">INPUTS</span></span>

## <span data-ttu-id="07a9e-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07a9e-125">OUTPUTS</span></span>

### <span data-ttu-id="07a9e-126">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="07a9e-126">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="07a9e-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="07a9e-127">NOTES</span></span>

## <span data-ttu-id="07a9e-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07a9e-128">RELATED LINKS</span></span>

[<span data-ttu-id="07a9e-129">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="07a9e-129">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="07a9e-130">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="07a9e-130">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


