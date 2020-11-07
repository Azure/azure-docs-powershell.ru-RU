---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
ms.openlocfilehash: 00d7bb2c58abfa466b0c4843eb480b43b08b3d90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733815"
---
# <span data-ttu-id="7337f-101">Get-AzureRmRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="7337f-101">Get-AzureRmRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="7337f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7337f-102">SYNOPSIS</span></span>
<span data-ttu-id="7337f-103">Проверяет, является ли резервная копия вашего ресурса ARM.</span><span class="sxs-lookup"><span data-stu-id="7337f-103">Checks whether your ARM resource is backed up or not.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7337f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7337f-104">SYNTAX</span></span>

### <span data-ttu-id="7337f-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7337f-105">Name (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7337f-106">Номер</span><span class="sxs-lookup"><span data-stu-id="7337f-106">Id</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7337f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7337f-107">DESCRIPTION</span></span>
<span data-ttu-id="7337f-108">Команда возвращает пустое значение (null), если указанный ресурс не защищен ни в одном из хранилищ служб восстановления в подписке.</span><span class="sxs-lookup"><span data-stu-id="7337f-108">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="7337f-109">Если он защищен, то будут возвращены сведения о своем хранилище.</span><span class="sxs-lookup"><span data-stu-id="7337f-109">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="7337f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7337f-110">EXAMPLES</span></span>

### <span data-ttu-id="7337f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7337f-111">Example 1</span></span>
```
PS C:\> $status = Get-AzureRmRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzureRmRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzureRmRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="7337f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7337f-112">PARAMETERS</span></span>

### <span data-ttu-id="7337f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7337f-113">-DefaultProfile</span></span>
<span data-ttu-id="7337f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7337f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7337f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7337f-115">-Name</span></span>
<span data-ttu-id="7337f-116">Имя ресурса Azure, элемент которого необходимо проверить, если он уже защищен некоторым хранилищем служб восстановления в подписке.</span><span class="sxs-lookup"><span data-stu-id="7337f-116">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="7337f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7337f-117">-ResourceGroupName</span></span>
<span data-ttu-id="7337f-118">Имя группы ресурсов для ресурса Azure, элемент которого должен быть установлен, если он уже защищен некоторым хранилищем RecoveryServices в подписке.</span><span class="sxs-lookup"><span data-stu-id="7337f-118">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="7337f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7337f-119">-ResourceId</span></span>
<span data-ttu-id="7337f-120">Идентификатор ресурса Azure, элемент которого должен быть проверен, если он уже защищен некоторым хранилищем RecoveryServices в подписке.</span><span class="sxs-lookup"><span data-stu-id="7337f-120">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7337f-121">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="7337f-121">-Type</span></span>
<span data-ttu-id="7337f-122">Имя ресурса Azure, элемент которого необходимо проверить, если он уже защищен некоторым хранилищем служб восстановления в подписке.</span><span class="sxs-lookup"><span data-stu-id="7337f-122">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7337f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7337f-123">CommonParameters</span></span>
<span data-ttu-id="7337f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7337f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7337f-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7337f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7337f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7337f-126">INPUTS</span></span>

### <span data-ttu-id="7337f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7337f-127">System.String</span></span>

## <span data-ttu-id="7337f-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7337f-128">OUTPUTS</span></span>

### <span data-ttu-id="7337f-129">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="7337f-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="7337f-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7337f-130">NOTES</span></span>

## <span data-ttu-id="7337f-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7337f-131">RELATED LINKS</span></span>
