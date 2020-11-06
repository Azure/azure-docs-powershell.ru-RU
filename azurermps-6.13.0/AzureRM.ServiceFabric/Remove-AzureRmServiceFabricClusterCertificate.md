---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 088f90af1ce80bdda390de1ce62a9d38581344aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563991"
---
# <span data-ttu-id="a5172-101">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a5172-101">Remove-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="a5172-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5172-102">SYNOPSIS</span></span>
<span data-ttu-id="a5172-103">Удаление сертификата кластера из использования для системы безопасности кластера.</span><span class="sxs-lookup"><span data-stu-id="a5172-103">Remove a cluster certificate from being used for cluster security.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5172-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5172-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5172-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5172-105">DESCRIPTION</span></span>
<span data-ttu-id="a5172-106">С помощью **Remove-AzureRmServiceFabricClusterCertificate** удалите сертификат кластера из кластера, если в нем уже используется другой действительный сертификат.</span><span class="sxs-lookup"><span data-stu-id="a5172-106">Use **Remove-AzureRmServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="a5172-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5172-107">EXAMPLES</span></span>

### <span data-ttu-id="a5172-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a5172-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="a5172-109">Эта команда удаляет сертификат с отпечатком 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, который используется для безопасности кластера.</span><span class="sxs-lookup"><span data-stu-id="a5172-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="a5172-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5172-110">PARAMETERS</span></span>

### <span data-ttu-id="a5172-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5172-111">-DefaultProfile</span></span>
<span data-ttu-id="a5172-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5172-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5172-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a5172-113">-Name</span></span>
<span data-ttu-id="a5172-114">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="a5172-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a5172-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5172-115">-ResourceGroupName</span></span>
<span data-ttu-id="a5172-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a5172-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a5172-117">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="a5172-117">-Thumbprint</span></span>
<span data-ttu-id="a5172-118">Укажите отпечаток кластера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a5172-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="a5172-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5172-119">-Confirm</span></span>
<span data-ttu-id="a5172-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a5172-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5172-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5172-121">-WhatIf</span></span>
<span data-ttu-id="a5172-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a5172-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5172-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a5172-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5172-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5172-124">CommonParameters</span></span>
<span data-ttu-id="a5172-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5172-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5172-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5172-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5172-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5172-127">INPUTS</span></span>

### <span data-ttu-id="a5172-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a5172-128">System.String</span></span>
<span data-ttu-id="a5172-129">Параметры: Thumbprint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5172-129">Parameters: Thumbprint (ByValue)</span></span>

## <span data-ttu-id="a5172-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5172-130">OUTPUTS</span></span>

### <span data-ttu-id="a5172-131">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a5172-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a5172-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5172-132">NOTES</span></span>

## <span data-ttu-id="a5172-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5172-133">RELATED LINKS</span></span>
