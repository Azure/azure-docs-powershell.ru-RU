---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231913"
---
# <span data-ttu-id="d5f08-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d5f08-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="d5f08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5f08-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f08-103">Получите сведения о ресурсах кластера.</span><span class="sxs-lookup"><span data-stu-id="d5f08-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="d5f08-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d5f08-104">SYNTAX</span></span>

### <span data-ttu-id="d5f08-105">BySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5f08-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f08-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d5f08-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5f08-107">ByName</span><span class="sxs-lookup"><span data-stu-id="d5f08-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5f08-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5f08-108">DESCRIPTION</span></span>
<span data-ttu-id="d5f08-109">Сведения **о ресурсах кластера будет получать get-AzServiceFabricCluster.**</span><span class="sxs-lookup"><span data-stu-id="d5f08-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="d5f08-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d5f08-110">EXAMPLES</span></span>

### <span data-ttu-id="d5f08-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d5f08-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="d5f08-112">Эта команда получит сведения о ресурсах кластера для кластера "МойCluster".</span><span class="sxs-lookup"><span data-stu-id="d5f08-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="d5f08-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5f08-113">PARAMETERS</span></span>

### <span data-ttu-id="d5f08-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f08-114">-DefaultProfile</span></span>
<span data-ttu-id="d5f08-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5f08-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5f08-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d5f08-116">-Name</span></span>
<span data-ttu-id="d5f08-117">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="d5f08-117">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f08-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5f08-118">-ResourceGroupName</span></span>
<span data-ttu-id="d5f08-119">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5f08-119">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f08-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f08-120">CommonParameters</span></span>
<span data-ttu-id="d5f08-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5f08-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f08-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5f08-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f08-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5f08-123">INPUTS</span></span>

### <span data-ttu-id="d5f08-124">System.String</span><span class="sxs-lookup"><span data-stu-id="d5f08-124">System.String</span></span>

## <span data-ttu-id="d5f08-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5f08-125">OUTPUTS</span></span>

### <span data-ttu-id="d5f08-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="d5f08-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="d5f08-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d5f08-127">NOTES</span></span>

## <span data-ttu-id="d5f08-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5f08-128">RELATED LINKS</span></span>
