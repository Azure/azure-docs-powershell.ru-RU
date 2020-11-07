---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 65e5e507259198cdacc69ff0764b4f4f18bf9077
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733967"
---
# <span data-ttu-id="72dec-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="72dec-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="72dec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72dec-102">SYNOPSIS</span></span>
<span data-ttu-id="72dec-103">Создание политики репликации восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="72dec-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72dec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72dec-104">SYNTAX</span></span>

### <span data-ttu-id="72dec-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="72dec-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72dec-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="72dec-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72dec-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72dec-107">DESCRIPTION</span></span>
<span data-ttu-id="72dec-108">Командлет **New-AzureRmSiteRecoveryPolicy** создает политику репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="72dec-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="72dec-109">Политика репликации используется для указания параметров репликации, таких как частота репликации и количество точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="72dec-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="72dec-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72dec-110">EXAMPLES</span></span>

## <span data-ttu-id="72dec-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72dec-111">PARAMETERS</span></span>

### <span data-ttu-id="72dec-112">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="72dec-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="72dec-113">Указывает частоту для моментального снимка, совместимого с приложением, в часах.</span><span class="sxs-lookup"><span data-stu-id="72dec-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dec-114">-Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="72dec-114">-Authentication</span></span>
<span data-ttu-id="72dec-115">Указывает тип используемой проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="72dec-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="72dec-116">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="72dec-116">Valid values are:</span></span>

- <span data-ttu-id="72dec-117">См</span><span class="sxs-lookup"><span data-stu-id="72dec-117">Certificate</span></span>
-  <span data-ttu-id="72dec-118">Использованием</span><span class="sxs-lookup"><span data-stu-id="72dec-118">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dec-119">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="72dec-119">-Compression</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dec-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72dec-120">-DefaultProfile</span></span>
<span data-ttu-id="72dec-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72dec-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72dec-122">-Шифрование</span><span class="sxs-lookup"><span data-stu-id="72dec-122">-Encryption</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dec-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="72dec-123">-Name</span></span>
<span data-ttu-id="72dec-124">Задает понятное имя, идентифицирующее политику репликации восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="72dec-124">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dec-125">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="72dec-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="72dec-126">Указывает идентификатор учетной записи хранилища Azure целевого объекта репликации.</span><span class="sxs-lookup"><span data-stu-id="72dec-126">Specifies the Azure storage account ID of the replication target.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dec-127">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="72dec-127">-RecoveryPoints</span></span>
<span data-ttu-id="72dec-128">Задает количество часов в часах для хранения точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="72dec-128">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dec-129">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="72dec-129">-ReplicaDeletion</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dec-130">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="72dec-130">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="72dec-131">Указывает периодичность репликации (в секундах).</span><span class="sxs-lookup"><span data-stu-id="72dec-131">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="72dec-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="72dec-132">Valid values are:</span></span>

- <span data-ttu-id="72dec-133">30</span><span class="sxs-lookup"><span data-stu-id="72dec-133">30</span></span>
- <span data-ttu-id="72dec-134">300</span><span class="sxs-lookup"><span data-stu-id="72dec-134">300</span></span>
- <span data-ttu-id="72dec-135">900</span><span class="sxs-lookup"><span data-stu-id="72dec-135">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dec-136">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="72dec-136">-ReplicationMethod</span></span>
<span data-ttu-id="72dec-137">Указывает метод репликации.</span><span class="sxs-lookup"><span data-stu-id="72dec-137">Specifies the replication method.</span></span>
<span data-ttu-id="72dec-138">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="72dec-138">Valid values are:</span></span>

- <span data-ttu-id="72dec-139">Онлайн</span><span class="sxs-lookup"><span data-stu-id="72dec-139">Online</span></span>
- <span data-ttu-id="72dec-140">Доступ</span><span class="sxs-lookup"><span data-stu-id="72dec-140">Offline</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dec-141">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="72dec-141">-ReplicationPort</span></span>
<span data-ttu-id="72dec-142">Указывает порт, используемый для репликации.</span><span class="sxs-lookup"><span data-stu-id="72dec-142">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dec-143">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="72dec-143">-ReplicationProvider</span></span>
<span data-ttu-id="72dec-144">Указывает поставщика репликации.</span><span class="sxs-lookup"><span data-stu-id="72dec-144">Specifies the replication provider.</span></span>
<span data-ttu-id="72dec-145">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="72dec-145">Valid values are:</span></span>

- <span data-ttu-id="72dec-146">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="72dec-146">HyperVReplica2012R2</span></span>
- <span data-ttu-id="72dec-147">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="72dec-147">HyperVReplica2012</span></span>
- <span data-ttu-id="72dec-148">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="72dec-148">HyperVReplicaAzure</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dec-149">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="72dec-149">-ReplicationStartTime</span></span>
<span data-ttu-id="72dec-150">Указывает время начала репликации.</span><span class="sxs-lookup"><span data-stu-id="72dec-150">Specifies the replication start time.</span></span>
<span data-ttu-id="72dec-151">Оно должно быть не позже, чем 24 часа, начиная с начала задания.</span><span class="sxs-lookup"><span data-stu-id="72dec-151">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72dec-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72dec-152">CommonParameters</span></span>
<span data-ttu-id="72dec-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72dec-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72dec-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72dec-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72dec-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72dec-155">INPUTS</span></span>

### <span data-ttu-id="72dec-156">Ничего</span><span class="sxs-lookup"><span data-stu-id="72dec-156">None</span></span>
<span data-ttu-id="72dec-157">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="72dec-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72dec-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72dec-158">OUTPUTS</span></span>

## <span data-ttu-id="72dec-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="72dec-159">NOTES</span></span>

## <span data-ttu-id="72dec-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72dec-160">RELATED LINKS</span></span>

[<span data-ttu-id="72dec-161">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="72dec-161">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="72dec-162">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="72dec-162">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
