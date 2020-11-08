---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247020"
---
# <span data-ttu-id="c39f8-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c39f8-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="c39f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c39f8-102">SYNOPSIS</span></span>
<span data-ttu-id="c39f8-103">Получение сведений о ресурсе кластера.</span><span class="sxs-lookup"><span data-stu-id="c39f8-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="c39f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c39f8-104">SYNTAX</span></span>

### <span data-ttu-id="c39f8-105">BySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c39f8-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c39f8-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c39f8-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c39f8-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c39f8-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c39f8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c39f8-108">DESCRIPTION</span></span>
<span data-ttu-id="c39f8-109">Данные **Get-AzServiceFabricCluster** будут получать сведения о ресурсе кластера.</span><span class="sxs-lookup"><span data-stu-id="c39f8-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="c39f8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c39f8-110">EXAMPLES</span></span>

### <span data-ttu-id="c39f8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c39f8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="c39f8-112">Эта команда получит сведения о ресурсе кластера для кластера "myCluster".</span><span class="sxs-lookup"><span data-stu-id="c39f8-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="c39f8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c39f8-113">PARAMETERS</span></span>

### <span data-ttu-id="c39f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c39f8-114">-DefaultProfile</span></span>
<span data-ttu-id="c39f8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c39f8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c39f8-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c39f8-116">-Name</span></span>
<span data-ttu-id="c39f8-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="c39f8-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="c39f8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c39f8-118">-ResourceGroupName</span></span>
<span data-ttu-id="c39f8-119">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c39f8-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c39f8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39f8-120">CommonParameters</span></span>
<span data-ttu-id="c39f8-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c39f8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c39f8-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c39f8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39f8-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c39f8-123">INPUTS</span></span>

### <span data-ttu-id="c39f8-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c39f8-124">System.String</span></span>

## <span data-ttu-id="c39f8-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c39f8-125">OUTPUTS</span></span>

### <span data-ttu-id="c39f8-126">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="c39f8-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c39f8-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="c39f8-127">NOTES</span></span>

## <span data-ttu-id="c39f8-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c39f8-128">RELATED LINKS</span></span>
