---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: 1f841d8cb49463f1ca9ce9198fc6173bb7efe506
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242765"
---
# <span data-ttu-id="935a0-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="935a0-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="935a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="935a0-102">SYNOPSIS</span></span>
<span data-ttu-id="935a0-103">Добавление профиля безопасности в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="935a0-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="935a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="935a0-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="935a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="935a0-105">DESCRIPTION</span></span>
<span data-ttu-id="935a0-106">Профиль безопасности используется для создания защищенного кластера, kerberizing его.</span><span class="sxs-lookup"><span data-stu-id="935a0-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="935a0-107">Профиль безопасности включает конфигурацию, связанную с присоединением кластера к домену Active Directory.</span><span class="sxs-lookup"><span data-stu-id="935a0-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="935a0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="935a0-108">EXAMPLES</span></span>

### <span data-ttu-id="935a0-109">Пример 1: Добавление профиля безопасности в объект конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="935a0-109">Example 1: Add security profile to the cluster configuration object</span></span>
```
PS C:\> #Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="935a0-110">Эта команда добавляет значение профиля безопасности в кластер с именем "-Hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="935a0-110">This command adds a security profile value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="935a0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="935a0-111">PARAMETERS</span></span>

### <span data-ttu-id="935a0-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="935a0-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="935a0-113">Различающиеся имена групп Active Directory, которые будут доступны в Ambari и Ranger</span><span class="sxs-lookup"><span data-stu-id="935a0-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="935a0-114">-Config</span><span class="sxs-lookup"><span data-stu-id="935a0-114">-Config</span></span>
<span data-ttu-id="935a0-115">Указывает объект конфигурации кластера HDInsight, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="935a0-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="935a0-116">Этот объект создается командлетом New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="935a0-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="935a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935a0-117">-DefaultProfile</span></span>
<span data-ttu-id="935a0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="935a0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="935a0-119">-Domain (домен)</span><span class="sxs-lookup"><span data-stu-id="935a0-119">-Domain</span></span>
<span data-ttu-id="935a0-120">Домен Active Directory для кластера</span><span class="sxs-lookup"><span data-stu-id="935a0-120">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="935a0-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="935a0-121">-DomainUserCredential</span></span>
<span data-ttu-id="935a0-122">Учетные данные учетной записи пользователя домена с достаточными разрешениями для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="935a0-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="935a0-123">Имя пользователя должно быть в user@domain формате</span><span class="sxs-lookup"><span data-stu-id="935a0-123">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="935a0-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="935a0-124">-LdapsUrls</span></span>
<span data-ttu-id="935a0-125">URL-адреса одного или нескольких серверов LDAP для службы каталогов Active Directory</span><span class="sxs-lookup"><span data-stu-id="935a0-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="935a0-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="935a0-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="935a0-127">Отличительное имя подразделения в службе каталогов Active Directory, где будут создаваться учетные записи пользователей и компьютеров.</span><span class="sxs-lookup"><span data-stu-id="935a0-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="935a0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="935a0-128">-Confirm</span></span>
<span data-ttu-id="935a0-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="935a0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="935a0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="935a0-130">-WhatIf</span></span>
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

### <span data-ttu-id="935a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935a0-131">CommonParameters</span></span>
<span data-ttu-id="935a0-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="935a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935a0-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="935a0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935a0-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="935a0-134">INPUTS</span></span>

### <span data-ttu-id="935a0-135">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="935a0-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
## <span data-ttu-id="935a0-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="935a0-136">OUTPUTS</span></span>

### <span data-ttu-id="935a0-137">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="935a0-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>
## <span data-ttu-id="935a0-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="935a0-138">NOTES</span></span>

## <span data-ttu-id="935a0-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="935a0-139">RELATED LINKS</span></span>
