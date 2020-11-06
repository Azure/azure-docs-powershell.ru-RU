---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8aba5d85e11a6494c4362de4d729c5e7b64106fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567890"
---
# <span data-ttu-id="27b3d-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="27b3d-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="27b3d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="27b3d-103">Создание плана восстановления сайта в восстановлении сайта.</span><span class="sxs-lookup"><span data-stu-id="27b3d-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27b3d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27b3d-104">SYNTAX</span></span>

### <span data-ttu-id="27b3d-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27b3d-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27b3d-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="27b3d-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27b3d-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="27b3d-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27b3d-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="27b3d-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27b3d-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="27b3d-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27b3d-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="27b3d-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27b3d-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27b3d-111">DESCRIPTION</span></span>
<span data-ttu-id="27b3d-112">Командлет **New-AzureRmSiteRecoveryRecoveryPlan** создает план восстановления в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="27b3d-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="27b3d-113">План восстановления собирает виртуальные машины в группе в целях перемещения при сбое и восстановления.</span><span class="sxs-lookup"><span data-stu-id="27b3d-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="27b3d-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27b3d-114">EXAMPLES</span></span>

### <span data-ttu-id="27b3d-115">Пример 1: Добавление плана восстановления к хранилищу для восстановления сайта</span><span class="sxs-lookup"><span data-stu-id="27b3d-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="27b3d-116">Эта команда добавляет план восстановления с именем RecoveryPlan.xml в хранилище Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="27b3d-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="27b3d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27b3d-117">PARAMETERS</span></span>

### <span data-ttu-id="27b3d-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="27b3d-118">-Azure</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b3d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b3d-119">-DefaultProfile</span></span>
<span data-ttu-id="27b3d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27b3d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27b3d-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="27b3d-121">-FailoverDeploymentModel</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b3d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="27b3d-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b3d-123">-Path</span><span class="sxs-lookup"><span data-stu-id="27b3d-123">-Path</span></span>
<span data-ttu-id="27b3d-124">Задает путь к файлу плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="27b3d-124">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b3d-125">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="27b3d-125">-PrimaryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b3d-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="27b3d-126">-PrimaryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b3d-127">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="27b3d-127">-PrimarySite</span></span>
```yaml
Type: ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b3d-128">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="27b3d-128">-ProtectionEntityList</span></span>
```yaml
Type: ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27b3d-129">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="27b3d-129">-RecoveryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b3d-130">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="27b3d-130">-RecoveryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b3d-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="27b3d-131">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27b3d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b3d-132">CommonParameters</span></span>
<span data-ttu-id="27b3d-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27b3d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b3d-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27b3d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b3d-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27b3d-135">INPUTS</span></span>

### <span data-ttu-id="27b3d-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="27b3d-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="27b3d-137">Параметр "ProtectionEntityList" принимает значение типа "ASRProtectionEntity []" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="27b3d-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="27b3d-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="27b3d-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="27b3d-139">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem []" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="27b3d-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="27b3d-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27b3d-140">OUTPUTS</span></span>

## <span data-ttu-id="27b3d-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="27b3d-141">NOTES</span></span>

## <span data-ttu-id="27b3d-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27b3d-142">RELATED LINKS</span></span>

[<span data-ttu-id="27b3d-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="27b3d-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="27b3d-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="27b3d-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="27b3d-145">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="27b3d-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


