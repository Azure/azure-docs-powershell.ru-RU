---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: e876e1a7beeee19cd68ac629eb08d48356f98da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734505"
---
# <span data-ttu-id="e04e2-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="e04e2-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="e04e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e04e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e04e2-103">Создание политики репликации восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="e04e2-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e04e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e04e2-104">SYNTAX</span></span>

### <span data-ttu-id="e04e2-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e04e2-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e04e2-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="e04e2-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e04e2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e04e2-107">DESCRIPTION</span></span>
<span data-ttu-id="e04e2-108">Командлет **New-AzureRmSiteRecoveryPolicy** создает политику репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="e04e2-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="e04e2-109">Политика репликации используется для указания параметров репликации, таких как частота репликации и количество точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="e04e2-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="e04e2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e04e2-110">EXAMPLES</span></span>

## <span data-ttu-id="e04e2-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e04e2-111">PARAMETERS</span></span>

### <span data-ttu-id="e04e2-112">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="e04e2-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="e04e2-113">Указывает частоту для моментального снимка, совместимого с приложением, в часах.</span><span class="sxs-lookup"><span data-stu-id="e04e2-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04e2-114">-Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="e04e2-114">-Authentication</span></span>
<span data-ttu-id="e04e2-115">Указывает тип используемой проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e04e2-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="e04e2-116">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e04e2-116">Valid values are:</span></span>

- <span data-ttu-id="e04e2-117">См</span><span class="sxs-lookup"><span data-stu-id="e04e2-117">Certificate</span></span>
-  <span data-ttu-id="e04e2-118">Использованием</span><span class="sxs-lookup"><span data-stu-id="e04e2-118">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04e2-119">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="e04e2-119">-Compression</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04e2-120">-Шифрование</span><span class="sxs-lookup"><span data-stu-id="e04e2-120">-Encryption</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04e2-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e04e2-121">-Name</span></span>
<span data-ttu-id="e04e2-122">Задает понятное имя, идентифицирующее политику репликации восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="e04e2-122">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="e04e2-123">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e04e2-123">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="e04e2-124">Указывает идентификатор учетной записи хранилища Azure целевого объекта репликации.</span><span class="sxs-lookup"><span data-stu-id="e04e2-124">Specifies the Azure storage account ID of the replication target.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04e2-125">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="e04e2-125">-RecoveryPoints</span></span>
<span data-ttu-id="e04e2-126">Задает количество часов в часах для хранения точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="e04e2-126">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04e2-127">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="e04e2-127">-ReplicaDeletion</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04e2-128">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="e04e2-128">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="e04e2-129">Указывает периодичность репликации (в секундах).</span><span class="sxs-lookup"><span data-stu-id="e04e2-129">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="e04e2-130">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e04e2-130">Valid values are:</span></span>

- <span data-ttu-id="e04e2-131">30</span><span class="sxs-lookup"><span data-stu-id="e04e2-131">30</span></span>
- <span data-ttu-id="e04e2-132">300</span><span class="sxs-lookup"><span data-stu-id="e04e2-132">300</span></span>
- <span data-ttu-id="e04e2-133">900</span><span class="sxs-lookup"><span data-stu-id="e04e2-133">900</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04e2-134">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="e04e2-134">-ReplicationMethod</span></span>
<span data-ttu-id="e04e2-135">Указывает метод репликации.</span><span class="sxs-lookup"><span data-stu-id="e04e2-135">Specifies the replication method.</span></span>
<span data-ttu-id="e04e2-136">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e04e2-136">Valid values are:</span></span>

- <span data-ttu-id="e04e2-137">Онлайн</span><span class="sxs-lookup"><span data-stu-id="e04e2-137">Online</span></span>
- <span data-ttu-id="e04e2-138">Доступ</span><span class="sxs-lookup"><span data-stu-id="e04e2-138">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04e2-139">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="e04e2-139">-ReplicationPort</span></span>
<span data-ttu-id="e04e2-140">Указывает порт, используемый для репликации.</span><span class="sxs-lookup"><span data-stu-id="e04e2-140">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04e2-141">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="e04e2-141">-ReplicationProvider</span></span>
<span data-ttu-id="e04e2-142">Указывает поставщика репликации.</span><span class="sxs-lookup"><span data-stu-id="e04e2-142">Specifies the replication provider.</span></span>
<span data-ttu-id="e04e2-143">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e04e2-143">Valid values are:</span></span>

- <span data-ttu-id="e04e2-144">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="e04e2-144">HyperVReplica2012R2</span></span>
- <span data-ttu-id="e04e2-145">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="e04e2-145">HyperVReplica2012</span></span>
- <span data-ttu-id="e04e2-146">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="e04e2-146">HyperVReplicaAzure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04e2-147">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="e04e2-147">-ReplicationStartTime</span></span>
<span data-ttu-id="e04e2-148">Указывает время начала репликации.</span><span class="sxs-lookup"><span data-stu-id="e04e2-148">Specifies the replication start time.</span></span>
<span data-ttu-id="e04e2-149">Оно должно быть не позже, чем 24 часа, начиная с начала задания.</span><span class="sxs-lookup"><span data-stu-id="e04e2-149">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04e2-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e04e2-150">-DefaultProfile</span></span>
<span data-ttu-id="e04e2-151">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e04e2-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e04e2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04e2-152">CommonParameters</span></span>
<span data-ttu-id="e04e2-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e04e2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04e2-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e04e2-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04e2-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e04e2-155">INPUTS</span></span>

## <span data-ttu-id="e04e2-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e04e2-156">OUTPUTS</span></span>

## <span data-ttu-id="e04e2-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="e04e2-157">NOTES</span></span>

## <span data-ttu-id="e04e2-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e04e2-158">RELATED LINKS</span></span>

[<span data-ttu-id="e04e2-159">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="e04e2-159">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="e04e2-160">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="e04e2-160">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
