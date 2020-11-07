---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 590f2470cacd349eb8f0467ce37e7c15ab5a9321
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903777"
---
# <span data-ttu-id="dc6cc-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dc6cc-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="dc6cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc6cc-102">SYNOPSIS</span></span>
<span data-ttu-id="dc6cc-103">Получение сведений о приложении "структура служб".</span><span class="sxs-lookup"><span data-stu-id="dc6cc-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="dc6cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc6cc-104">SYNTAX</span></span>

### <span data-ttu-id="dc6cc-105">ByResourceGroupAndCluster (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc6cc-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc6cc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dc6cc-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc6cc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dc6cc-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc6cc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc6cc-108">DESCRIPTION</span></span>
<span data-ttu-id="dc6cc-109">Этот командлет получает сведения о приложении в заданной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="dc6cc-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="dc6cc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc6cc-110">EXAMPLES</span></span>

### <span data-ttu-id="dc6cc-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc6cc-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="dc6cc-112">В этом примере показано получение сведений о ресурсах приложения для приложения "testApp".</span><span class="sxs-lookup"><span data-stu-id="dc6cc-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="dc6cc-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dc6cc-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="dc6cc-114">В этом примере показано получение списка приложений в кластере "testCluster".</span><span class="sxs-lookup"><span data-stu-id="dc6cc-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="dc6cc-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc6cc-115">PARAMETERS</span></span>

### <span data-ttu-id="dc6cc-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="dc6cc-116">-ClusterName</span></span>
<span data-ttu-id="dc6cc-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="dc6cc-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="dc6cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc6cc-118">-DefaultProfile</span></span>
<span data-ttu-id="dc6cc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc6cc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc6cc-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc6cc-120">-Name</span></span>
<span data-ttu-id="dc6cc-121">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="dc6cc-121">Specify the name of the application.</span></span>

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

### <span data-ttu-id="dc6cc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc6cc-122">-ResourceGroupName</span></span>
<span data-ttu-id="dc6cc-123">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc6cc-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="dc6cc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc6cc-124">-ResourceId</span></span>
<span data-ttu-id="dc6cc-125">ИД ресурса ARM приложения.</span><span class="sxs-lookup"><span data-stu-id="dc6cc-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="dc6cc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc6cc-126">CommonParameters</span></span>
<span data-ttu-id="dc6cc-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc6cc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc6cc-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc6cc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc6cc-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc6cc-129">INPUTS</span></span>

### <span data-ttu-id="dc6cc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dc6cc-130">System.String</span></span>

## <span data-ttu-id="dc6cc-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc6cc-131">OUTPUTS</span></span>

### <span data-ttu-id="dc6cc-132">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="dc6cc-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="dc6cc-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc6cc-133">NOTES</span></span>

## <span data-ttu-id="dc6cc-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc6cc-134">RELATED LINKS</span></span>
