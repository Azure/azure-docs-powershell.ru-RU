---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 9595f3fc3062d6afdd5b5bbfab74f297b39b3f6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236092"
---
# <span data-ttu-id="1ac70-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ac70-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="1ac70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ac70-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac70-103">Получает политики защиты резервных копий для хранилища.</span><span class="sxs-lookup"><span data-stu-id="1ac70-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="1ac70-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1ac70-104">SYNTAX</span></span>

### <span data-ttu-id="1ac70-105">NoParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1ac70-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ac70-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="1ac70-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ac70-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="1ac70-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ac70-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="1ac70-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ac70-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ac70-109">DESCRIPTION</span></span>
<span data-ttu-id="1ac70-110">Для хранилища с использованием **cmdlet Get-AzRecoveryServicesBackupProtectionPolicy** получает политики защиты резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac70-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="1ac70-111">Прежде чем использовать текущий Set-AzRecoveryServicesVaultContext, задате контекст хранилища с помощью Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="1ac70-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1ac70-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1ac70-112">EXAMPLES</span></span>

### <span data-ttu-id="1ac70-113">Пример 1. Все политики в хранилище</span><span class="sxs-lookup"><span data-stu-id="1ac70-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="1ac70-114">Эта команда получает все политики защиты, созданные в хранилище.</span><span class="sxs-lookup"><span data-stu-id="1ac70-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="1ac70-115">Пример 2. Получить определенную политику</span><span class="sxs-lookup"><span data-stu-id="1ac70-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="1ac70-116">Эта команда получает политику защиты с именем DefaultPolicy, а затем сохраняет ее в переменной $Pol безопасности.</span><span class="sxs-lookup"><span data-stu-id="1ac70-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="1ac70-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ac70-117">PARAMETERS</span></span>

### <span data-ttu-id="1ac70-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="1ac70-118">-BackupManagementType</span></span>
<span data-ttu-id="1ac70-119">Класс защищенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ac70-119">The class of resources being protected.</span></span> <span data-ttu-id="1ac70-120">В настоящее время для этого командлета поддерживаются такие значения: AzureVM, AzureStorage, AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="1ac70-120">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureStorage, AzureWorkload, MAB

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac70-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac70-121">-DefaultProfile</span></span>
<span data-ttu-id="1ac70-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac70-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ac70-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1ac70-123">-Name</span></span>
<span data-ttu-id="1ac70-124">Указывает имя политики.</span><span class="sxs-lookup"><span data-stu-id="1ac70-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="1ac70-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1ac70-125">-VaultId</span></span>
<span data-ttu-id="1ac70-126">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="1ac70-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1ac70-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="1ac70-127">-WorkloadType</span></span>
<span data-ttu-id="1ac70-128">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ac70-128">Workload type of the resource.</span></span> <span data-ttu-id="1ac70-129">В настоящее время поддерживаются значения AzureVM, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="1ac70-129">The current supported values are AzureVM, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="1ac70-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac70-130">CommonParameters</span></span>
<span data-ttu-id="1ac70-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ac70-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac70-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ac70-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac70-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ac70-133">INPUTS</span></span>

### <span data-ttu-id="1ac70-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1ac70-134">System.String</span></span>

## <span data-ttu-id="1ac70-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1ac70-135">OUTPUTS</span></span>

### <span data-ttu-id="1ac70-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="1ac70-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="1ac70-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1ac70-137">NOTES</span></span>

## <span data-ttu-id="1ac70-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ac70-138">RELATED LINKS</span></span>

[<span data-ttu-id="1ac70-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ac70-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1ac70-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ac70-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1ac70-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ac70-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


