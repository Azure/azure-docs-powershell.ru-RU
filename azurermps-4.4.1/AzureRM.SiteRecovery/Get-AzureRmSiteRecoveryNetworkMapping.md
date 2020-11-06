---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 01AE09A8-B779-475A-9E86-776E0774E89E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: d9a1e26691ab0ea1be04365747f97d8fc6111672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565124"
---
# <span data-ttu-id="57917-101">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="57917-101">Get-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="57917-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57917-102">SYNOPSIS</span></span>
<span data-ttu-id="57917-103">Получение сведений о сопоставлениях сети восстановления сайта для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="57917-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57917-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57917-104">SYNTAX</span></span>

### <span data-ttu-id="57917-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57917-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57917-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="57917-106">EnterpriseToEnterprise</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57917-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="57917-107">EnterpriseToAzure</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> [-Azure]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57917-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="57917-108">EnterpriseToAzureLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-Azure] -PrimaryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57917-109">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="57917-109">EnterpriseToEnterpriseLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57917-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57917-110">DESCRIPTION</span></span>
<span data-ttu-id="57917-111">Командлет **Get-AzureRmSiteRecoveryNetworkMapping** получает сведения о сопоставлениях сети Azure Site Recovery для текущего хранилища сайта для восстановления.</span><span class="sxs-lookup"><span data-stu-id="57917-111">The **Get-AzureRmSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="57917-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57917-112">EXAMPLES</span></span>

## <span data-ttu-id="57917-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57917-113">PARAMETERS</span></span>

### <span data-ttu-id="57917-114">-Azure</span><span class="sxs-lookup"><span data-stu-id="57917-114">-Azure</span></span>
<span data-ttu-id="57917-115">Указывает на то, что команда получает список сетевых сопоставлений для сетей на основном сервере, сопоставленных с виртуальными сетями Azure.</span><span class="sxs-lookup"><span data-stu-id="57917-115">Indicates that the command gets a list of network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57917-116">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="57917-116">-PrimaryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57917-117">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="57917-117">-PrimaryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToAzureLegacy, EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57917-118">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="57917-118">-RecoveryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57917-119">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="57917-119">-RecoveryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57917-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57917-120">-DefaultProfile</span></span>
<span data-ttu-id="57917-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57917-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57917-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57917-122">CommonParameters</span></span>
<span data-ttu-id="57917-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57917-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57917-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57917-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57917-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57917-125">INPUTS</span></span>

### <span data-ttu-id="57917-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="57917-126">ASRFabric</span></span>
<span data-ttu-id="57917-127">Параметр "PrimaryFabric" принимает значение типа "ASRFabric" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="57917-127">Parameter 'PrimaryFabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="57917-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="57917-128">ASRServer</span></span>
<span data-ttu-id="57917-129">Параметр "PrimaryServer" принимает значение типа "ASRServer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="57917-129">Parameter 'PrimaryServer' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="57917-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57917-130">OUTPUTS</span></span>

### <span data-ttu-id="57917-131">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetworkMapping]</span><span class="sxs-lookup"><span data-stu-id="57917-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping]</span></span>

## <span data-ttu-id="57917-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="57917-132">NOTES</span></span>

## <span data-ttu-id="57917-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57917-133">RELATED LINKS</span></span>

[<span data-ttu-id="57917-134">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="57917-134">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="57917-135">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="57917-135">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
