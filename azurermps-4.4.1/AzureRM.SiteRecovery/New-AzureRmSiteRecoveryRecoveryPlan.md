---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: fa308c0961d11320964d7c31a7d77642e968b09b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733317"
---
# <span data-ttu-id="06213-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="06213-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="06213-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06213-102">SYNOPSIS</span></span>
<span data-ttu-id="06213-103">Создание плана восстановления сайта в восстановлении сайта.</span><span class="sxs-lookup"><span data-stu-id="06213-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06213-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06213-104">SYNTAX</span></span>

### <span data-ttu-id="06213-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="06213-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06213-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="06213-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06213-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="06213-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06213-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="06213-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06213-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="06213-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06213-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="06213-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06213-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06213-111">DESCRIPTION</span></span>
<span data-ttu-id="06213-112">Командлет **New-AzureRmSiteRecoveryRecoveryPlan** создает план восстановления в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="06213-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="06213-113">План восстановления собирает виртуальные машины в группе в целях перемещения при сбое и восстановления.</span><span class="sxs-lookup"><span data-stu-id="06213-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="06213-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06213-114">EXAMPLES</span></span>

### <span data-ttu-id="06213-115">Пример 1: Добавление плана восстановления к хранилищу для восстановления сайта</span><span class="sxs-lookup"><span data-stu-id="06213-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="06213-116">Эта команда добавляет план восстановления с именем RecoveryPlan.xml в хранилище Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="06213-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="06213-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06213-117">PARAMETERS</span></span>

### <span data-ttu-id="06213-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="06213-118">-Azure</span></span>
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

### <span data-ttu-id="06213-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="06213-119">-FailoverDeploymentModel</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06213-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="06213-120">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06213-121">-Path</span><span class="sxs-lookup"><span data-stu-id="06213-121">-Path</span></span>
<span data-ttu-id="06213-122">Задает путь к файлу плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="06213-122">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06213-123">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="06213-123">-PrimaryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06213-124">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="06213-124">-PrimaryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06213-125">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="06213-125">-PrimarySite</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06213-126">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="06213-126">-ProtectionEntityList</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06213-127">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="06213-127">-RecoveryFabric</span></span>
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

### <span data-ttu-id="06213-128">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="06213-128">-RecoveryServer</span></span>
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

### <span data-ttu-id="06213-129">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="06213-129">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06213-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06213-130">-DefaultProfile</span></span>
<span data-ttu-id="06213-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06213-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06213-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06213-132">CommonParameters</span></span>
<span data-ttu-id="06213-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06213-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06213-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06213-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06213-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06213-135">INPUTS</span></span>

### <span data-ttu-id="06213-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="06213-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="06213-137">Параметр "ProtectionEntityList" принимает значение типа "ASRProtectionEntity []" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="06213-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="06213-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="06213-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="06213-139">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem []" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="06213-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="06213-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06213-140">OUTPUTS</span></span>

## <span data-ttu-id="06213-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="06213-141">NOTES</span></span>

## <span data-ttu-id="06213-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06213-142">RELATED LINKS</span></span>

[<span data-ttu-id="06213-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="06213-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="06213-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="06213-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="06213-145">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="06213-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


