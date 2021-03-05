---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 59f8723470707a644e426bd9559a8e982f731e6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005523"
---
# <span data-ttu-id="6110b-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6110b-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="6110b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6110b-102">SYNOPSIS</span></span>
<span data-ttu-id="6110b-103">Удалите сертификат кластера из использования для защиты кластера.</span><span class="sxs-lookup"><span data-stu-id="6110b-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="6110b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6110b-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6110b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6110b-105">DESCRIPTION</span></span>
<span data-ttu-id="6110b-106">Используйте **Remove-AzServiceFabricClusterCertificate,** чтобы удалить сертификат кластера из кластера, если в кластере уже есть другой допустимый сертификат.</span><span class="sxs-lookup"><span data-stu-id="6110b-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="6110b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6110b-107">EXAMPLES</span></span>

### <span data-ttu-id="6110b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6110b-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="6110b-109">Эта команда удаляет сертификат с thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A из-за использования в целях безопасности кластера.</span><span class="sxs-lookup"><span data-stu-id="6110b-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="6110b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6110b-110">PARAMETERS</span></span>

### <span data-ttu-id="6110b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6110b-111">-DefaultProfile</span></span>
<span data-ttu-id="6110b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6110b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6110b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6110b-113">-Name</span></span>
<span data-ttu-id="6110b-114">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="6110b-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6110b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6110b-115">-ResourceGroupName</span></span>
<span data-ttu-id="6110b-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6110b-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6110b-117">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="6110b-117">-Thumbprint</span></span>
<span data-ttu-id="6110b-118">Укажите препечатку кластера, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6110b-118">Specify the cluster thumbprint which to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6110b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6110b-119">-Confirm</span></span>
<span data-ttu-id="6110b-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6110b-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6110b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6110b-121">-WhatIf</span></span>
<span data-ttu-id="6110b-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6110b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6110b-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6110b-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6110b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6110b-124">CommonParameters</span></span>
<span data-ttu-id="6110b-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6110b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6110b-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6110b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6110b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6110b-127">INPUTS</span></span>

### <span data-ttu-id="6110b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6110b-128">System.String</span></span>

## <span data-ttu-id="6110b-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6110b-129">OUTPUTS</span></span>

### <span data-ttu-id="6110b-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="6110b-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6110b-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6110b-131">NOTES</span></span>

## <span data-ttu-id="6110b-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6110b-132">RELATED LINKS</span></span>
