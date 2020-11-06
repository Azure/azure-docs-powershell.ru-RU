---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 76238516065dffc7a8a38ee6ad025f67d54b47c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562292"
---
# <span data-ttu-id="43869-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="43869-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="43869-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43869-102">SYNOPSIS</span></span>
<span data-ttu-id="43869-103">Включение резервного копирования для элемента с указанной политикой защиты резервной копии.</span><span class="sxs-lookup"><span data-stu-id="43869-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43869-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43869-104">SYNTAX</span></span>

### <span data-ttu-id="43869-105">AzureVMComputeEnableProtection (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43869-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43869-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="43869-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43869-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="43869-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43869-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43869-108">DESCRIPTION</span></span>
<span data-ttu-id="43869-109">Командлет **Enable-AzureRmRecoveryServicesBackupProtection** задает политику защиты резервного копирования Azure для элемента.</span><span class="sxs-lookup"><span data-stu-id="43869-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="43869-110">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="43869-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="43869-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43869-111">EXAMPLES</span></span>

### <span data-ttu-id="43869-112">Пример 1: Включение защиты резервных копий для элемента</span><span class="sxs-lookup"><span data-stu-id="43869-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="43869-113">Первый командлет получает объект политики по умолчанию, а затем сохраняет его в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="43869-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="43869-114">Второй командлет задает политику защиты резервного копирования для виртуальной машины ARM с именем V2VM, используя политику в $Pol.</span><span class="sxs-lookup"><span data-stu-id="43869-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="43869-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43869-115">PARAMETERS</span></span>

### <span data-ttu-id="43869-116">-Item</span><span class="sxs-lookup"><span data-stu-id="43869-116">-Item</span></span>
<span data-ttu-id="43869-117">Указывает элемент резервного копирования, для которого этот командлет включит защиту.</span><span class="sxs-lookup"><span data-stu-id="43869-117">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="43869-118">Чтобы получить **AzureRmRecoveryServicesBackupItem** , используйте командлет Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="43869-118">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43869-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43869-119">-Name</span></span>
<span data-ttu-id="43869-120">Указывает имя элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="43869-120">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43869-121">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="43869-121">-Policy</span></span>
<span data-ttu-id="43869-122">Задает политику защиты, которую этот командлет связывает с элементом.</span><span class="sxs-lookup"><span data-stu-id="43869-122">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="43869-123">Чтобы получить объект **AzureRmRecoveryServicesBackupProtectionPolicy** , используйте командлет Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="43869-123">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43869-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43869-124">-ResourceGroupName</span></span>
<span data-ttu-id="43869-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43869-125">Specifies the name of the resource group.</span></span>
<span data-ttu-id="43869-126">Указывайте этот параметр только для виртуальных машин ARM.</span><span class="sxs-lookup"><span data-stu-id="43869-126">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43869-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="43869-127">-ServiceName</span></span>
<span data-ttu-id="43869-128">Указывает имя службы.</span><span class="sxs-lookup"><span data-stu-id="43869-128">Specifies the service name.</span></span>
<span data-ttu-id="43869-129">Указывайте этот параметр только для виртуальных машин ASM.</span><span class="sxs-lookup"><span data-stu-id="43869-129">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43869-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43869-130">-DefaultProfile</span></span>
<span data-ttu-id="43869-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43869-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43869-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43869-132">CommonParameters</span></span>
<span data-ttu-id="43869-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43869-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43869-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43869-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43869-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43869-135">INPUTS</span></span>

### <span data-ttu-id="43869-136">ItemBase</span><span class="sxs-lookup"><span data-stu-id="43869-136">ItemBase</span></span>
<span data-ttu-id="43869-137">Параметр "элемент" принимает значение типа "ItemBase" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="43869-137">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="43869-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43869-138">OUTPUTS</span></span>

### <span data-ttu-id="43869-139">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="43869-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="43869-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="43869-140">NOTES</span></span>

## <span data-ttu-id="43869-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43869-141">RELATED LINKS</span></span>

[<span data-ttu-id="43869-142">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="43869-142">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="43869-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="43869-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


