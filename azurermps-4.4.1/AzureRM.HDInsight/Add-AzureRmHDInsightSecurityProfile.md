---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
ms.openlocfilehash: 7ea9f9d9bb07cae6db62c51b9d496f7117eee700
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568066"
---
# <span data-ttu-id="899cd-101">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="899cd-101">Add-AzureRmHDInsightSecurityProfile</span></span>

## <span data-ttu-id="899cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="899cd-102">SYNOPSIS</span></span>
<span data-ttu-id="899cd-103">Добавляет profileto безопасности объекта конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="899cd-103">Adds a security profileto a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="899cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="899cd-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="899cd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="899cd-105">DESCRIPTION</span></span>
<span data-ttu-id="899cd-106">Профиль безопасности используется для создания защищенного кластера, kerberizing его.</span><span class="sxs-lookup"><span data-stu-id="899cd-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="899cd-107">Профиль безопасности включает конфигурацию, связанную с присоединением кластера к домену Active Directory.</span><span class="sxs-lookup"><span data-stu-id="899cd-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="899cd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="899cd-108">EXAMPLES</span></span>

### <span data-ttu-id="899cd-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="899cd-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="899cd-110">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="899cd-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="899cd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="899cd-111">PARAMETERS</span></span>

### <span data-ttu-id="899cd-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="899cd-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="899cd-113">Различающиеся имена групп Active Directory, которые будут доступны в Ambari и Ranger</span><span class="sxs-lookup"><span data-stu-id="899cd-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="899cd-114">-Config</span><span class="sxs-lookup"><span data-stu-id="899cd-114">-Config</span></span>
<span data-ttu-id="899cd-115">Указывает объект конфигурации кластера HDInsight, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="899cd-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="899cd-116">Этот объект создается командлетом New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="899cd-116">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="899cd-117">-Domain (домен)</span><span class="sxs-lookup"><span data-stu-id="899cd-117">-Domain</span></span>
<span data-ttu-id="899cd-118">Домен Active Directory для кластера</span><span class="sxs-lookup"><span data-stu-id="899cd-118">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="899cd-119">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="899cd-119">-DomainUserCredential</span></span>
<span data-ttu-id="899cd-120">Учетные данные учетной записи пользователя домена с достаточными разрешениями для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="899cd-120">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="899cd-121">Имя пользователя должно быть в user@domain формате</span><span class="sxs-lookup"><span data-stu-id="899cd-121">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="899cd-122">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="899cd-122">-LdapsUrls</span></span>
<span data-ttu-id="899cd-123">URL-адреса одного или нескольких серверов LDAP для службы каталогов Active Directory</span><span class="sxs-lookup"><span data-stu-id="899cd-123">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="899cd-124">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="899cd-124">-OrganizationalUnitDN</span></span>
<span data-ttu-id="899cd-125">Отличительное имя подразделения в службе каталогов Active Directory, где будут создаваться учетные записи пользователей и компьютеров.</span><span class="sxs-lookup"><span data-stu-id="899cd-125">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="899cd-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="899cd-126">-Confirm</span></span>
<span data-ttu-id="899cd-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="899cd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="899cd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="899cd-128">-WhatIf</span></span>
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

### <span data-ttu-id="899cd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="899cd-129">-DefaultProfile</span></span>
<span data-ttu-id="899cd-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="899cd-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="899cd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899cd-131">CommonParameters</span></span>
<span data-ttu-id="899cd-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="899cd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="899cd-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="899cd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899cd-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="899cd-134">INPUTS</span></span>

### <span data-ttu-id="899cd-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="899cd-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="899cd-136">Параметр config принимает значение типа "AzureHDInsightConfig" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="899cd-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="899cd-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="899cd-137">OUTPUTS</span></span>

### <span data-ttu-id="899cd-138">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="899cd-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="899cd-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="899cd-139">NOTES</span></span>

## <span data-ttu-id="899cd-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="899cd-140">RELATED LINKS</span></span>

