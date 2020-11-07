---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4BF1E20A-46EA-48E2-8C7A-F121AE6815AF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 36f5c6e535cc67029fac7c951cbc6dbbe3c73091
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733969"
---
# <span data-ttu-id="d3003-101">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d3003-101">New-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="d3003-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3003-102">SYNOPSIS</span></span>
<span data-ttu-id="d3003-103">Создание сопоставления между виртуальными сетями.</span><span class="sxs-lookup"><span data-stu-id="d3003-103">Creates a mapping between virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3003-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3003-104">SYNTAX</span></span>

### <span data-ttu-id="d3003-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d3003-105">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3003-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="d3003-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork> -AzureVMNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3003-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3003-107">DESCRIPTION</span></span>
<span data-ttu-id="d3003-108">Командлет **New-AzureRMSiteRecoveryNetworkMapping** создает сопоставление между двумя виртуальными сетями и возвращает задание Azure Site Recovery для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="d3003-108">The **New-AzureRMSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="d3003-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3003-109">EXAMPLES</span></span>

## <span data-ttu-id="d3003-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3003-110">PARAMETERS</span></span>

### <span data-ttu-id="d3003-111">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="d3003-111">-AzureVMNetworkId</span></span>
<span data-ttu-id="d3003-112">Указывает идентификатор виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="d3003-112">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3003-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3003-113">-DefaultProfile</span></span>
<span data-ttu-id="d3003-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3003-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3003-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d3003-115">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3003-116">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="d3003-116">-PrimaryNetwork</span></span>
<span data-ttu-id="d3003-117">Указывает основной объект сети.</span><span class="sxs-lookup"><span data-stu-id="d3003-117">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3003-118">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="d3003-118">-RecoveryNetwork</span></span>
<span data-ttu-id="d3003-119">Указывает сетевой объект для восстановления.</span><span class="sxs-lookup"><span data-stu-id="d3003-119">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3003-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3003-120">CommonParameters</span></span>
<span data-ttu-id="d3003-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3003-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3003-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3003-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3003-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3003-123">INPUTS</span></span>

### <span data-ttu-id="d3003-124">ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="d3003-124">ASRNetwork</span></span>
<span data-ttu-id="d3003-125">Параметр "PrimaryNetwork" принимает значение типа "ASRNetwork" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3003-125">Parameter 'PrimaryNetwork' accepts value of type 'ASRNetwork' from the pipeline</span></span>

## <span data-ttu-id="d3003-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3003-126">OUTPUTS</span></span>

### <span data-ttu-id="d3003-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d3003-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d3003-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3003-128">NOTES</span></span>

## <span data-ttu-id="d3003-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3003-129">RELATED LINKS</span></span>

[<span data-ttu-id="d3003-130">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d3003-130">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="d3003-131">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d3003-131">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
