---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 688ee9f8679a427d53319147e7d13fc9e1305277
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245864"
---
# <span data-ttu-id="c0826-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="c0826-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="c0826-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0826-102">SYNOPSIS</span></span>
<span data-ttu-id="c0826-103">Удаление сертификата кластера из использования для системы безопасности кластера.</span><span class="sxs-lookup"><span data-stu-id="c0826-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="c0826-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0826-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0826-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0826-105">DESCRIPTION</span></span>
<span data-ttu-id="c0826-106">С помощью **Remove-AzServiceFabricClusterCertificate** удалите сертификат кластера из кластера, если в нем уже используется другой действительный сертификат.</span><span class="sxs-lookup"><span data-stu-id="c0826-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="c0826-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0826-107">EXAMPLES</span></span>

### <span data-ttu-id="c0826-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0826-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="c0826-109">Эта команда удаляет сертификат с отпечатком 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, который используется для безопасности кластера.</span><span class="sxs-lookup"><span data-stu-id="c0826-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="c0826-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0826-110">PARAMETERS</span></span>

### <span data-ttu-id="c0826-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0826-111">-DefaultProfile</span></span>
<span data-ttu-id="c0826-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0826-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0826-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0826-113">-Name</span></span>
<span data-ttu-id="c0826-114">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="c0826-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c0826-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0826-115">-ResourceGroupName</span></span>
<span data-ttu-id="c0826-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0826-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c0826-117">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="c0826-117">-Thumbprint</span></span>
<span data-ttu-id="c0826-118">Укажите отпечаток кластера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c0826-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="c0826-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0826-119">-Confirm</span></span>
<span data-ttu-id="c0826-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c0826-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0826-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0826-121">-WhatIf</span></span>
<span data-ttu-id="c0826-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c0826-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0826-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c0826-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0826-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0826-124">CommonParameters</span></span>
<span data-ttu-id="c0826-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0826-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0826-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0826-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0826-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0826-127">INPUTS</span></span>

### <span data-ttu-id="c0826-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c0826-128">System.String</span></span>

## <span data-ttu-id="c0826-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0826-129">OUTPUTS</span></span>

### <span data-ttu-id="c0826-130">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="c0826-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c0826-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0826-131">NOTES</span></span>

## <span data-ttu-id="c0826-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0826-132">RELATED LINKS</span></span>
