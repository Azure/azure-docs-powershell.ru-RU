---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: c44fea946f98c6ac19e77e7012910afac37bff7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397791"
---
# <span data-ttu-id="2c4e5-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="2c4e5-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="2c4e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c4e5-102">SYNOPSIS</span></span>
<span data-ttu-id="2c4e5-103">Добавляет профиль безопасности в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="2c4e5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2c4e5-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -DomainResourceId <String>
 -DomainUserCredential <PSCredential> [-OrganizationalUnitDN <String>] -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c4e5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c4e5-105">DESCRIPTION</span></span>
<span data-ttu-id="2c4e5-106">Профиль безопасности используется для создания защищенного кластера путем керберизации.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="2c4e5-107">Профиль безопасности содержит конфигурацию, связанную с присоединением кластера к домену Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="2c4e5-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2c4e5-108">EXAMPLES</span></span>

### <span data-ttu-id="2c4e5-109">Пример 1. Добавление профиля безопасности к объекту конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="2c4e5-109">Example 1: Add security profile to the cluster configuration object</span></span>
```
PS C:\> #Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

#Security profile info
PS C:\> $domain="sampledomain.onmicrosoft.com"
PS C:\> $domainUser="sample.user@sampledomain.onmicrosoft.com"
PS C:\> $domainPassword=ConvertTo-SecureString "domainPassword" -AsPlainText -Force
PS C:\> $domainUserCredential=New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
PS C:\> $organizationalUnitDN="ou=testunitdn"
PS C:\> $ldapsUrls=("ldaps://sampledomain.onmicrosoft.com:636","ldaps://sampledomain.onmicrosoft.com:389")
PS C:\> $clusterUsersGroupDNs=("groupdn1","groupdn2")

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightSecurityProfile `
                -Domain $domain `
                -DomainUserCredential $domainUserCredential `
                -OrganizationalUnitDN $organizationalUnitDN `
                -LdapsUrls $ldapsUrls `
                -ClusterUsersGroupDNs $clusterUsersGroupDNs `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="2c4e5-110">Эта команда добавляет значение профиля безопасности в кластер с именем your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-110">This command adds a security profile value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2c4e5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c4e5-111">PARAMETERS</span></span>

### <span data-ttu-id="2c4e5-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="2c4e5-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="2c4e5-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span><span class="sxs-lookup"><span data-stu-id="2c4e5-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4e5-114">-Config</span><span class="sxs-lookup"><span data-stu-id="2c4e5-114">-Config</span></span>
<span data-ttu-id="2c4e5-115">Определяет объект конфигурации кластера HDInsight, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="2c4e5-116">Этот объект создается с помощью New-AzHDInsightClusterConfig-управления.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c4e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c4e5-117">-DefaultProfile</span></span>
<span data-ttu-id="2c4e5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2c4e5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c4e5-119">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="2c4e5-119">-DomainResourceId</span></span>
<span data-ttu-id="2c4e5-120">ИД ресурса домена Active Directory для кластера.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-120">Active Directory domain resource id for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4e5-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="2c4e5-121">-DomainUserCredential</span></span>
<span data-ttu-id="2c4e5-122">Учетная запись пользователя домена с достаточными разрешениями для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="2c4e5-123">Имя пользователя должно быть в user@domain формате</span><span class="sxs-lookup"><span data-stu-id="2c4e5-123">Username should be in user@domain format</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4e5-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="2c4e5-124">-LdapsUrls</span></span>
<span data-ttu-id="2c4e5-125">URL-адреса одного или нескольких LDAPS-серверов для Active Directory</span><span class="sxs-lookup"><span data-stu-id="2c4e5-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4e5-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="2c4e5-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="2c4e5-127">Различается имя подразделения в Active Directory, в котором будут созданы учетные записи пользователей и компьютеров</span><span class="sxs-lookup"><span data-stu-id="2c4e5-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4e5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c4e5-128">-Confirm</span></span>
<span data-ttu-id="2c4e5-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4e5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c4e5-130">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4e5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c4e5-131">CommonParameters</span></span>
<span data-ttu-id="2c4e5-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c4e5-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c4e5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c4e5-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c4e5-134">INPUTS</span></span>

### <span data-ttu-id="2c4e5-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="2c4e5-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
## <span data-ttu-id="2c4e5-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2c4e5-136">OUTPUTS</span></span>

### <span data-ttu-id="2c4e5-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="2c4e5-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>
## <span data-ttu-id="2c4e5-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2c4e5-138">NOTES</span></span>

## <span data-ttu-id="2c4e5-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c4e5-139">RELATED LINKS</span></span>
