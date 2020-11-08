---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: 1e10fe2aa534e236c99468ec672e6a0eeadae469
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074719"
---
# <span data-ttu-id="e3b5e-101">Get-AzRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="e3b5e-101">Get-AzRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="e3b5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b5e-103">Проверяет, является ли резервная копия вашего ресурса ARM.</span><span class="sxs-lookup"><span data-stu-id="e3b5e-103">Checks whether your ARM resource is backed up or not.</span></span>

## <span data-ttu-id="e3b5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3b5e-104">SYNTAX</span></span>

### <span data-ttu-id="e3b5e-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3b5e-105">Name (Default)</span></span>
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3b5e-106">IdWorkload</span><span class="sxs-lookup"><span data-stu-id="e3b5e-106">IdWorkload</span></span>
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3b5e-107">Номер</span><span class="sxs-lookup"><span data-stu-id="e3b5e-107">Id</span></span>
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3b5e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3b5e-108">DESCRIPTION</span></span>
<span data-ttu-id="e3b5e-109">Команда возвращает пустое значение (null), если указанный ресурс не защищен ни в одном из хранилищ служб восстановления в подписке.</span><span class="sxs-lookup"><span data-stu-id="e3b5e-109">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="e3b5e-110">Если он защищен, то будут возвращены сведения о своем хранилище.</span><span class="sxs-lookup"><span data-stu-id="e3b5e-110">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="e3b5e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3b5e-111">EXAMPLES</span></span>

### <span data-ttu-id="e3b5e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e3b5e-112">Example 1</span></span>
```
PS C:\> $status = Get-AzRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="e3b5e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3b5e-113">PARAMETERS</span></span>

### <span data-ttu-id="e3b5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b5e-114">-DefaultProfile</span></span>
<span data-ttu-id="e3b5e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b5e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3b5e-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3b5e-116">-Name</span></span>
<span data-ttu-id="e3b5e-117">Имя ресурса Azure, элемент которого необходимо проверить, если он уже защищен некоторым хранилищем служб восстановления в подписке.</span><span class="sxs-lookup"><span data-stu-id="e3b5e-117">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b5e-118">-ProtectableObjectName</span><span class="sxs-lookup"><span data-stu-id="e3b5e-118">-ProtectableObjectName</span></span>
<span data-ttu-id="e3b5e-119">Имя ресурса Azure, элемент которого необходимо проверить, если он уже защищен некоторым хранилищем служб восстановления в подписке.</span><span class="sxs-lookup"><span data-stu-id="e3b5e-119">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b5e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b5e-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3b5e-121">Имя группы ресурсов для ресурса Azure, элемент которого должен быть установлен, если он уже защищен некоторым хранилищем RecoveryServices в подписке.</span><span class="sxs-lookup"><span data-stu-id="e3b5e-121">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b5e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3b5e-122">-ResourceId</span></span>
<span data-ttu-id="e3b5e-123">Идентификатор ресурса Azure, элемент которого должен быть проверен, если он уже защищен некоторым хранилищем RecoveryServices в подписке.</span><span class="sxs-lookup"><span data-stu-id="e3b5e-123">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload, Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b5e-124">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="e3b5e-124">-Type</span></span>
<span data-ttu-id="e3b5e-125">Имя ресурса Azure, элемент которого необходимо проверить, если он уже защищен некоторым хранилищем служб восстановления в подписке.</span><span class="sxs-lookup"><span data-stu-id="e3b5e-125">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, IdWorkload
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b5e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b5e-126">CommonParameters</span></span>
<span data-ttu-id="e3b5e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3b5e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b5e-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3b5e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b5e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3b5e-129">INPUTS</span></span>

### <span data-ttu-id="e3b5e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e3b5e-130">System.String</span></span>

## <span data-ttu-id="e3b5e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3b5e-131">OUTPUTS</span></span>

### <span data-ttu-id="e3b5e-132">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="e3b5e-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="e3b5e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3b5e-133">NOTES</span></span>

## <span data-ttu-id="e3b5e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3b5e-134">RELATED LINKS</span></span>
