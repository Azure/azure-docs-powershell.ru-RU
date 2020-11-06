---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/get-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
ms.openlocfilehash: ee8420a8869e1056dc0ee3d942b811c3f70d545d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566641"
---
# <span data-ttu-id="06cad-101">Get-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="06cad-101">Get-AzureRmAks</span></span>

## <span data-ttu-id="06cad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06cad-102">SYNOPSIS</span></span>
<span data-ttu-id="06cad-103">Перечислите Kubernetes управляемые кластеры.</span><span class="sxs-lookup"><span data-stu-id="06cad-103">List Kubernetes managed clusters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06cad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06cad-104">SYNTAX</span></span>

### <span data-ttu-id="06cad-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="06cad-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06cad-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06cad-106">IdParameterSet</span></span>
```
Get-AzureRmAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06cad-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="06cad-107">NameParameterSet</span></span>
```
Get-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06cad-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06cad-108">DESCRIPTION</span></span>
<span data-ttu-id="06cad-109">Перечислите Kubernetes управляемые кластеры.</span><span class="sxs-lookup"><span data-stu-id="06cad-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="06cad-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06cad-110">EXAMPLES</span></span>

### <span data-ttu-id="06cad-111">Список всех кластеров Kubernetes</span><span class="sxs-lookup"><span data-stu-id="06cad-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzureRmAks
```

## <span data-ttu-id="06cad-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06cad-112">PARAMETERS</span></span>

### <span data-ttu-id="06cad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06cad-113">-DefaultProfile</span></span>
<span data-ttu-id="06cad-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06cad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06cad-115">-ID</span><span class="sxs-lookup"><span data-stu-id="06cad-115">-Id</span></span>
<span data-ttu-id="06cad-116">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="06cad-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06cad-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="06cad-117">-Name</span></span>
<span data-ttu-id="06cad-118">Имя управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="06cad-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06cad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06cad-119">-ResourceGroupName</span></span>
<span data-ttu-id="06cad-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="06cad-120">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06cad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06cad-121">CommonParameters</span></span>
<span data-ttu-id="06cad-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06cad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06cad-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06cad-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06cad-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06cad-124">INPUTS</span></span>

### <span data-ttu-id="06cad-125">System. String</span><span class="sxs-lookup"><span data-stu-id="06cad-125">System.String</span></span>

## <span data-ttu-id="06cad-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06cad-126">OUTPUTS</span></span>

### <span data-ttu-id="06cad-127">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="06cad-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="06cad-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster, Microsoft. Azure. Commands. AKS, Version = 0.0.0.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="06cad-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster, Microsoft.Azure.Commands.Aks, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="06cad-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="06cad-129">NOTES</span></span>

## <span data-ttu-id="06cad-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06cad-130">RELATED LINKS</span></span>
