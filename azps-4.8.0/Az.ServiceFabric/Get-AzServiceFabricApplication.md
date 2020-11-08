---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: c282ea9e902f26d010c2421339de68bc670e2f35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235327"
---
# <span data-ttu-id="1f073-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1f073-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="1f073-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f073-102">SYNOPSIS</span></span>
<span data-ttu-id="1f073-103">Получение сведений о приложении "структура служб".</span><span class="sxs-lookup"><span data-stu-id="1f073-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="1f073-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f073-104">SYNTAX</span></span>

### <span data-ttu-id="1f073-105">ByResourceGroupAndCluster (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f073-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f073-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1f073-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f073-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f073-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f073-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f073-108">DESCRIPTION</span></span>
<span data-ttu-id="1f073-109">Этот командлет получает сведения о приложении в заданной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="1f073-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="1f073-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f073-110">EXAMPLES</span></span>

### <span data-ttu-id="1f073-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f073-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="1f073-112">В этом примере показано получение сведений о ресурсах приложения для приложения "testApp".</span><span class="sxs-lookup"><span data-stu-id="1f073-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="1f073-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1f073-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="1f073-114">В этом примере показано получение списка приложений в кластере "testCluster".</span><span class="sxs-lookup"><span data-stu-id="1f073-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="1f073-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f073-115">PARAMETERS</span></span>

### <span data-ttu-id="1f073-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="1f073-116">-ClusterName</span></span>
<span data-ttu-id="1f073-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="1f073-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f073-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f073-118">-DefaultProfile</span></span>
<span data-ttu-id="1f073-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f073-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f073-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f073-120">-Name</span></span>
<span data-ttu-id="1f073-121">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="1f073-121">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f073-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f073-122">-ResourceGroupName</span></span>
<span data-ttu-id="1f073-123">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f073-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f073-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f073-124">-ResourceId</span></span>
<span data-ttu-id="1f073-125">ИД ресурса ARM приложения.</span><span class="sxs-lookup"><span data-stu-id="1f073-125">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f073-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f073-126">CommonParameters</span></span>
<span data-ttu-id="1f073-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f073-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f073-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f073-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f073-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f073-129">INPUTS</span></span>

### <span data-ttu-id="1f073-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1f073-130">System.String</span></span>

## <span data-ttu-id="1f073-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f073-131">OUTPUTS</span></span>

### <span data-ttu-id="1f073-132">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="1f073-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="1f073-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f073-133">NOTES</span></span>

## <span data-ttu-id="1f073-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f073-134">RELATED LINKS</span></span>
