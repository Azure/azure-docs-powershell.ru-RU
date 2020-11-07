---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 295cb5bad09584c16e1217e68d3fc80c5ebf8598
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904913"
---
# <span data-ttu-id="185f3-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="185f3-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="185f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="185f3-102">SYNOPSIS</span></span>
<span data-ttu-id="185f3-103">Получает политики защиты резервного копирования для хранилища.</span><span class="sxs-lookup"><span data-stu-id="185f3-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="185f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="185f3-104">SYNTAX</span></span>

### <span data-ttu-id="185f3-105">Параметр param (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="185f3-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="185f3-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="185f3-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="185f3-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="185f3-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="185f3-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="185f3-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="185f3-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="185f3-109">DESCRIPTION</span></span>
<span data-ttu-id="185f3-110">Командлет **Get-AzRecoveryServicesBackupProtectionPolicy** получает политики защиты резервных копий Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="185f3-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="185f3-111">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="185f3-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="185f3-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="185f3-112">EXAMPLES</span></span>

### <span data-ttu-id="185f3-113">Пример 1: получение всех политик в хранилище</span><span class="sxs-lookup"><span data-stu-id="185f3-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="185f3-114">Эта команда получает все политики защиты, созданные в хранилище.</span><span class="sxs-lookup"><span data-stu-id="185f3-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="185f3-115">Пример 2: получение определенной политики</span><span class="sxs-lookup"><span data-stu-id="185f3-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="185f3-116">Эта команда получает политику защиты с именем DefaultPolicy и сохраняет ее в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="185f3-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="185f3-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="185f3-117">PARAMETERS</span></span>

### <span data-ttu-id="185f3-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="185f3-118">-BackupManagementType</span></span>
<span data-ttu-id="185f3-119">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="185f3-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="185f3-120">В настоящее время поддерживается только AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="185f3-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="185f3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="185f3-121">-DefaultProfile</span></span>
<span data-ttu-id="185f3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="185f3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="185f3-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="185f3-123">-Name</span></span>
<span data-ttu-id="185f3-124">Указывает имя политики.</span><span class="sxs-lookup"><span data-stu-id="185f3-124">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="185f3-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="185f3-125">-VaultId</span></span>
<span data-ttu-id="185f3-126">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="185f3-126">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="185f3-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="185f3-127">-WorkloadType</span></span>
<span data-ttu-id="185f3-128">Указывает тип рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="185f3-128">Specifies the workload type.</span></span>
<span data-ttu-id="185f3-129">В настоящее время поддерживается только AzureVM, AzureFiles.</span><span class="sxs-lookup"><span data-stu-id="185f3-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="185f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="185f3-130">CommonParameters</span></span>
<span data-ttu-id="185f3-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="185f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="185f3-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="185f3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="185f3-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="185f3-133">INPUTS</span></span>

### <span data-ttu-id="185f3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="185f3-134">System.String</span></span>

## <span data-ttu-id="185f3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="185f3-135">OUTPUTS</span></span>

### <span data-ttu-id="185f3-136">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="185f3-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="185f3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="185f3-137">NOTES</span></span>

## <span data-ttu-id="185f3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="185f3-138">RELATED LINKS</span></span>

[<span data-ttu-id="185f3-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="185f3-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="185f3-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="185f3-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="185f3-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="185f3-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


