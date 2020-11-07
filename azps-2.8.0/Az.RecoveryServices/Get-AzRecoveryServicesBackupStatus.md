---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: cd3e3e2ad33cb01935a2594571145f0667c9a3e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904885"
---
# <span data-ttu-id="78bb3-101">Get-AzRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="78bb3-101">Get-AzRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="78bb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="78bb3-103">Проверяет, является ли резервная копия вашего ресурса ARM.</span><span class="sxs-lookup"><span data-stu-id="78bb3-103">Checks whether your ARM resource is backed up or not.</span></span>

## <span data-ttu-id="78bb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78bb3-104">SYNTAX</span></span>

### <span data-ttu-id="78bb3-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78bb3-105">Name (Default)</span></span>
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78bb3-106">IdWorkload</span><span class="sxs-lookup"><span data-stu-id="78bb3-106">IdWorkload</span></span>
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78bb3-107">Номер</span><span class="sxs-lookup"><span data-stu-id="78bb3-107">Id</span></span>
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78bb3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78bb3-108">DESCRIPTION</span></span>
<span data-ttu-id="78bb3-109">Команда возвращает пустое значение (null), если указанный ресурс не защищен ни в одном из хранилищ служб восстановления в подписке.</span><span class="sxs-lookup"><span data-stu-id="78bb3-109">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="78bb3-110">Если он защищен, то будут возвращены сведения о своем хранилище.</span><span class="sxs-lookup"><span data-stu-id="78bb3-110">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="78bb3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78bb3-111">EXAMPLES</span></span>

### <span data-ttu-id="78bb3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="78bb3-112">Example 1</span></span>
```
PS C:\> $status = Get-AzRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="78bb3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78bb3-113">PARAMETERS</span></span>

### <span data-ttu-id="78bb3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78bb3-114">-DefaultProfile</span></span>
<span data-ttu-id="78bb3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78bb3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78bb3-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="78bb3-116">-Name</span></span>
<span data-ttu-id="78bb3-117">Имя ресурса Azure, элемент которого необходимо проверить, если он уже защищен некоторым хранилищем служб восстановления в подписке.</span><span class="sxs-lookup"><span data-stu-id="78bb3-117">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="78bb3-118">-ProtectableObjectName</span><span class="sxs-lookup"><span data-stu-id="78bb3-118">-ProtectableObjectName</span></span>
<span data-ttu-id="78bb3-119">Имя ресурса Azure, элемент которого необходимо проверить, если он уже защищен некоторым хранилищем служб восстановления в подписке.</span><span class="sxs-lookup"><span data-stu-id="78bb3-119">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="78bb3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78bb3-120">-ResourceGroupName</span></span>
<span data-ttu-id="78bb3-121">Имя группы ресурсов для ресурса Azure, элемент которого должен быть установлен, если он уже защищен некоторым хранилищем RecoveryServices в подписке.</span><span class="sxs-lookup"><span data-stu-id="78bb3-121">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="78bb3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78bb3-122">-ResourceId</span></span>
<span data-ttu-id="78bb3-123">Идентификатор ресурса Azure, элемент которого должен быть проверен, если он уже защищен некоторым хранилищем RecoveryServices в подписке.</span><span class="sxs-lookup"><span data-stu-id="78bb3-123">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="78bb3-124">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="78bb3-124">-Type</span></span>
<span data-ttu-id="78bb3-125">Имя ресурса Azure, элемент которого необходимо проверить, если он уже защищен некоторым хранилищем служб восстановления в подписке.</span><span class="sxs-lookup"><span data-stu-id="78bb3-125">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="78bb3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78bb3-126">CommonParameters</span></span>
<span data-ttu-id="78bb3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78bb3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78bb3-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78bb3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78bb3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78bb3-129">INPUTS</span></span>

### <span data-ttu-id="78bb3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="78bb3-130">System.String</span></span>

## <span data-ttu-id="78bb3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78bb3-131">OUTPUTS</span></span>

### <span data-ttu-id="78bb3-132">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="78bb3-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="78bb3-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="78bb3-133">NOTES</span></span>

## <span data-ttu-id="78bb3-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78bb3-134">RELATED LINKS</span></span>
