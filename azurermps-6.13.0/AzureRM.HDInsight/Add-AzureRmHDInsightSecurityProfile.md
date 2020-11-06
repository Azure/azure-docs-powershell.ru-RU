---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
ms.openlocfilehash: 003072e6821561c78975d50fa627edf0f7fd120a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564516"
---
# <span data-ttu-id="d1f2f-101">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="d1f2f-101">Add-AzureRmHDInsightSecurityProfile</span></span>

## <span data-ttu-id="d1f2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f2f-103">Добавляет profileto безопасности объекта конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="d1f2f-103">Adds a security profileto a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1f2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1f2f-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1f2f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1f2f-105">DESCRIPTION</span></span>
<span data-ttu-id="d1f2f-106">Профиль безопасности используется для создания защищенного кластера, kerberizing его.</span><span class="sxs-lookup"><span data-stu-id="d1f2f-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="d1f2f-107">Профиль безопасности включает конфигурацию, связанную с присоединением кластера к домену Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d1f2f-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="d1f2f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1f2f-108">EXAMPLES</span></span>

### <span data-ttu-id="d1f2f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d1f2f-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d1f2f-110">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="d1f2f-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="d1f2f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1f2f-111">PARAMETERS</span></span>

### <span data-ttu-id="d1f2f-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="d1f2f-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="d1f2f-113">Различающиеся имена групп Active Directory, которые будут доступны в Ambari и Ranger</span><span class="sxs-lookup"><span data-stu-id="d1f2f-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="d1f2f-114">-Config</span><span class="sxs-lookup"><span data-stu-id="d1f2f-114">-Config</span></span>
<span data-ttu-id="d1f2f-115">Указывает объект конфигурации кластера HDInsight, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d1f2f-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="d1f2f-116">Этот объект создается командлетом New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="d1f2f-116">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="d1f2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f2f-117">-DefaultProfile</span></span>
<span data-ttu-id="d1f2f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d1f2f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1f2f-119">-Domain (домен)</span><span class="sxs-lookup"><span data-stu-id="d1f2f-119">-Domain</span></span>
<span data-ttu-id="d1f2f-120">Домен Active Directory для кластера</span><span class="sxs-lookup"><span data-stu-id="d1f2f-120">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="d1f2f-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="d1f2f-121">-DomainUserCredential</span></span>
<span data-ttu-id="d1f2f-122">Учетные данные учетной записи пользователя домена с достаточными разрешениями для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="d1f2f-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="d1f2f-123">Имя пользователя должно быть в user@domain формате</span><span class="sxs-lookup"><span data-stu-id="d1f2f-123">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="d1f2f-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="d1f2f-124">-LdapsUrls</span></span>
<span data-ttu-id="d1f2f-125">URL-адреса одного или нескольких серверов LDAP для службы каталогов Active Directory</span><span class="sxs-lookup"><span data-stu-id="d1f2f-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="d1f2f-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="d1f2f-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="d1f2f-127">Отличительное имя подразделения в службе каталогов Active Directory, где будут создаваться учетные записи пользователей и компьютеров.</span><span class="sxs-lookup"><span data-stu-id="d1f2f-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="d1f2f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1f2f-128">-Confirm</span></span>
<span data-ttu-id="d1f2f-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d1f2f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1f2f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1f2f-130">-WhatIf</span></span>
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

### <span data-ttu-id="d1f2f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f2f-131">CommonParameters</span></span>
<span data-ttu-id="d1f2f-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1f2f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f2f-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1f2f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f2f-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1f2f-134">INPUTS</span></span>

### <span data-ttu-id="d1f2f-135">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d1f2f-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="d1f2f-136">Параметры: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d1f2f-136">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="d1f2f-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1f2f-137">OUTPUTS</span></span>

### <span data-ttu-id="d1f2f-138">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="d1f2f-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="d1f2f-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1f2f-139">NOTES</span></span>

## <span data-ttu-id="d1f2f-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1f2f-140">RELATED LINKS</span></span>
