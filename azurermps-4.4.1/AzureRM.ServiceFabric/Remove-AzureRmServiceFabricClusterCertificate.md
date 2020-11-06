---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 0ef59a8071438fa1bfd1560ab2f2102722aa335f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562135"
---
# <span data-ttu-id="b3b72-101">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="b3b72-101">Remove-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="b3b72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3b72-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b72-103">Удаление сертификата кластера из использования для системы безопасности кластера.</span><span class="sxs-lookup"><span data-stu-id="b3b72-103">Remove a cluster certificate from being used for cluster security.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3b72-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3b72-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3b72-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3b72-105">DESCRIPTION</span></span>
<span data-ttu-id="b3b72-106">С помощью **Remove-AzureRmServiceFabricClusterCertificate** удалите сертификат кластера из кластера, если в нем уже используется другой действительный сертификат.</span><span class="sxs-lookup"><span data-stu-id="b3b72-106">Use **Remove-AzureRmServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="b3b72-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3b72-107">EXAMPLES</span></span>

### <span data-ttu-id="b3b72-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3b72-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="b3b72-109">Эта команда удаляет сертификат с отпечатком 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, который используется для безопасности кластера.</span><span class="sxs-lookup"><span data-stu-id="b3b72-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="b3b72-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3b72-110">PARAMETERS</span></span>

### <span data-ttu-id="b3b72-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b3b72-111">-Name</span></span>
<span data-ttu-id="b3b72-112">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="b3b72-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b3b72-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3b72-113">-ResourceGroupName</span></span>
<span data-ttu-id="b3b72-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b3b72-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b3b72-115">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="b3b72-115">-Thumbprint</span></span>
<span data-ttu-id="b3b72-116">Укажите отпечаток кластера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b3b72-116">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="b3b72-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3b72-117">-Confirm</span></span>
<span data-ttu-id="b3b72-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b3b72-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3b72-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3b72-119">-WhatIf</span></span>
<span data-ttu-id="b3b72-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b3b72-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3b72-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b3b72-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3b72-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b72-122">-DefaultProfile</span></span>
<span data-ttu-id="b3b72-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b72-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3b72-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b72-124">CommonParameters</span></span>
<span data-ttu-id="b3b72-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3b72-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b72-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3b72-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b72-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3b72-127">INPUTS</span></span>

### <span data-ttu-id="b3b72-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b3b72-128">System.String</span></span>

## <span data-ttu-id="b3b72-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3b72-129">OUTPUTS</span></span>

### <span data-ttu-id="b3b72-130">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="b3b72-130">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="b3b72-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3b72-131">NOTES</span></span>

## <span data-ttu-id="b3b72-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3b72-132">RELATED LINKS</span></span>

