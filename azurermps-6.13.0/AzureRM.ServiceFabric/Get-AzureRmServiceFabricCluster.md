---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 93240fe3deddbe5b6f8fb20d644a0e685cfdda11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567234"
---
# <span data-ttu-id="4fc94-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="4fc94-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="4fc94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4fc94-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc94-103">Получение сведений о ресурсе кластера.</span><span class="sxs-lookup"><span data-stu-id="4fc94-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fc94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4fc94-104">SYNTAX</span></span>

### <span data-ttu-id="4fc94-105">BySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4fc94-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc94-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4fc94-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4fc94-107">ByName</span><span class="sxs-lookup"><span data-stu-id="4fc94-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fc94-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fc94-108">DESCRIPTION</span></span>
<span data-ttu-id="4fc94-109">Данные **Get-AzureRmServiceFabricCluster** будут получать сведения о ресурсе кластера.</span><span class="sxs-lookup"><span data-stu-id="4fc94-109">The **Get-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="4fc94-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4fc94-110">EXAMPLES</span></span>

### <span data-ttu-id="4fc94-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4fc94-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="4fc94-112">Эта команда получит сведения о ресурсе кластера для кластера "myCluster".</span><span class="sxs-lookup"><span data-stu-id="4fc94-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="4fc94-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4fc94-113">PARAMETERS</span></span>

### <span data-ttu-id="4fc94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc94-114">-DefaultProfile</span></span>
<span data-ttu-id="4fc94-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4fc94-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fc94-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4fc94-116">-Name</span></span>
<span data-ttu-id="4fc94-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="4fc94-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4fc94-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fc94-118">-ResourceGroupName</span></span>
<span data-ttu-id="4fc94-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4fc94-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4fc94-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc94-120">CommonParameters</span></span>
<span data-ttu-id="4fc94-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4fc94-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc94-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc94-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc94-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4fc94-123">INPUTS</span></span>

### <span data-ttu-id="4fc94-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4fc94-124">System.String</span></span>

## <span data-ttu-id="4fc94-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fc94-125">OUTPUTS</span></span>

### <span data-ttu-id="4fc94-126">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="4fc94-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4fc94-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="4fc94-127">NOTES</span></span>

## <span data-ttu-id="4fc94-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fc94-128">RELATED LINKS</span></span>
