---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 645981bb7b2cb02a4bb54a03ccbb570ec31925dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569192"
---
# <span data-ttu-id="18b52-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="18b52-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="18b52-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18b52-102">SYNOPSIS</span></span>
<span data-ttu-id="18b52-103">Получение сведений о ресурсе кластера.</span><span class="sxs-lookup"><span data-stu-id="18b52-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18b52-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18b52-104">SYNTAX</span></span>

```
Get-AzureRmServiceFabricCluster [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18b52-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18b52-105">DESCRIPTION</span></span>
<span data-ttu-id="18b52-106">Элемент **Add-AzureRmServiceFabricCluster** будет получать сведения о ресурсе кластера.</span><span class="sxs-lookup"><span data-stu-id="18b52-106">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="18b52-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18b52-107">EXAMPLES</span></span>

### <span data-ttu-id="18b52-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="18b52-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="18b52-109">Эта команда получит сведения о ресурсе кластера для кластера "myCluster".</span><span class="sxs-lookup"><span data-stu-id="18b52-109">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="18b52-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18b52-110">PARAMETERS</span></span>

### <span data-ttu-id="18b52-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="18b52-111">-Name</span></span>
<span data-ttu-id="18b52-112">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="18b52-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b52-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b52-113">-ResourceGroupName</span></span>
<span data-ttu-id="18b52-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18b52-114">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b52-115">-DefaultProfile</span></span>
<span data-ttu-id="18b52-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18b52-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18b52-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b52-117">CommonParameters</span></span>
<span data-ttu-id="18b52-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18b52-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b52-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b52-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b52-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18b52-120">INPUTS</span></span>

### <span data-ttu-id="18b52-121">System. String</span><span class="sxs-lookup"><span data-stu-id="18b52-121">System.String</span></span>

## <span data-ttu-id="18b52-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18b52-122">OUTPUTS</span></span>

### <span data-ttu-id="18b52-123">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster, Microsoft. Azure. Commands = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="18b52-123">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="18b52-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="18b52-124">NOTES</span></span>

## <span data-ttu-id="18b52-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18b52-125">RELATED LINKS</span></span>

