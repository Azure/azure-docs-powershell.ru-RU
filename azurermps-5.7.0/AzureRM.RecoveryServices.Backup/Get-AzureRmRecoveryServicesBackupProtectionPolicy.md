---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 3220ef801ff86a3fb95a4595efd8c94330bfcba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732148"
---
# <span data-ttu-id="71eb5-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="71eb5-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="71eb5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="71eb5-103">Получает политики защиты резервного копирования для хранилища.</span><span class="sxs-lookup"><span data-stu-id="71eb5-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71eb5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71eb5-104">SYNTAX</span></span>

### <span data-ttu-id="71eb5-105">Параметр param (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71eb5-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71eb5-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="71eb5-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71eb5-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="71eb5-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71eb5-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="71eb5-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71eb5-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71eb5-109">DESCRIPTION</span></span>
<span data-ttu-id="71eb5-110">Командлет **Get-AzureRmRecoveryServicesBackupProtectionPolicy** получает политики защиты резервных копий Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="71eb5-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>

<span data-ttu-id="71eb5-111">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="71eb5-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="71eb5-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71eb5-112">EXAMPLES</span></span>

### <span data-ttu-id="71eb5-113">Пример 1: получение всех политик в хранилище</span><span class="sxs-lookup"><span data-stu-id="71eb5-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="71eb5-114">Эта команда получает все политики защиты, созданные в хранилище.</span><span class="sxs-lookup"><span data-stu-id="71eb5-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="71eb5-115">Пример 2: получение определенной политики</span><span class="sxs-lookup"><span data-stu-id="71eb5-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="71eb5-116">Эта команда получает политику защиты с именем DefaultPolicy и сохраняет ее в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="71eb5-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="71eb5-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71eb5-117">PARAMETERS</span></span>

### <span data-ttu-id="71eb5-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="71eb5-118">-BackupManagementType</span></span>
<span data-ttu-id="71eb5-119">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="71eb5-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="71eb5-120">В настоящее время поддерживается только AzureVM.</span><span class="sxs-lookup"><span data-stu-id="71eb5-120">Currently, only AzureVM is supported.</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71eb5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71eb5-121">-DefaultProfile</span></span>
<span data-ttu-id="71eb5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71eb5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71eb5-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71eb5-123">-Name</span></span>
<span data-ttu-id="71eb5-124">Указывает имя политики.</span><span class="sxs-lookup"><span data-stu-id="71eb5-124">Specifies the name of the policy.</span></span>

```yaml
Type: String
Parameter Sets: PolicyNameParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71eb5-125">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="71eb5-125">-WorkloadType</span></span>
<span data-ttu-id="71eb5-126">Указывает тип рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="71eb5-126">Specifies the workload type.</span></span>
<span data-ttu-id="71eb5-127">В настоящее время поддерживается только AzureVM.</span><span class="sxs-lookup"><span data-stu-id="71eb5-127">Currently, only AzureVM is supported.</span></span>

```yaml
Type: WorkloadType
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71eb5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71eb5-128">CommonParameters</span></span>
<span data-ttu-id="71eb5-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71eb5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71eb5-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71eb5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71eb5-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71eb5-131">INPUTS</span></span>

### <span data-ttu-id="71eb5-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="71eb5-132">None</span></span>
<span data-ttu-id="71eb5-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="71eb5-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71eb5-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71eb5-134">OUTPUTS</span></span>

### <span data-ttu-id="71eb5-135">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="71eb5-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="71eb5-136">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. PolicyBase]</span><span class="sxs-lookup"><span data-stu-id="71eb5-136">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase]</span></span>

## <span data-ttu-id="71eb5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="71eb5-137">NOTES</span></span>

## <span data-ttu-id="71eb5-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71eb5-138">RELATED LINKS</span></span>

[<span data-ttu-id="71eb5-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="71eb5-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="71eb5-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="71eb5-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="71eb5-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="71eb5-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


