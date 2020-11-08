---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245701"
---
# <span data-ttu-id="fee00-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="fee00-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="fee00-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fee00-102">SYNOPSIS</span></span>
<span data-ttu-id="fee00-103">Обновляет свойства хранилища.</span><span class="sxs-lookup"><span data-stu-id="fee00-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="fee00-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fee00-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fee00-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fee00-105">DESCRIPTION</span></span>
<span data-ttu-id="fee00-106">Командлет **Set-AzRecoveryServicesVaultProperty** обновляет свойства хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="fee00-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="fee00-107">Этот командлет возвращает обновленные свойства хранилища после текущей операции Set.</span><span class="sxs-lookup"><span data-stu-id="fee00-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="fee00-108">Использование свойств этого командлета хранилища, например Soft-Delete, может быть включено в любой момент.</span><span class="sxs-lookup"><span data-stu-id="fee00-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="fee00-109">Свойство **SoftDeleteFeatureState** хранилища можно отключить только в том случае, если в хранилище отсутствуют зарегистрированные контейнеры.</span><span class="sxs-lookup"><span data-stu-id="fee00-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="fee00-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fee00-110">EXAMPLES</span></span>

### <span data-ttu-id="fee00-111">Пример 1: обновление SoftDeleteFeatureState хранилища</span><span class="sxs-lookup"><span data-stu-id="fee00-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="fee00-112">Первая команда получает объект хранилища и сохраняет его в переменной $vault.</span><span class="sxs-lookup"><span data-stu-id="fee00-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="fee00-113">Вторая команда обновляет свойство SoftDeleteFeatureState хранилища на состояние Enabled (включено).</span><span class="sxs-lookup"><span data-stu-id="fee00-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="fee00-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fee00-114">PARAMETERS</span></span>

### <span data-ttu-id="fee00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee00-115">-DefaultProfile</span></span>
<span data-ttu-id="fee00-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fee00-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fee00-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="fee00-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="fee00-118">SoftDeleteFeatureState хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="fee00-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee00-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="fee00-119">-VaultId</span></span>
<span data-ttu-id="fee00-120">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="fee00-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fee00-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fee00-121">-Confirm</span></span>
<span data-ttu-id="fee00-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fee00-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee00-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee00-123">-WhatIf</span></span>
<span data-ttu-id="fee00-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fee00-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="fee00-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee00-125">CommonParameters</span></span>
<span data-ttu-id="fee00-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fee00-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee00-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fee00-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee00-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fee00-128">INPUTS</span></span>

### <span data-ttu-id="fee00-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fee00-129">System.String</span></span>

### <span data-ttu-id="fee00-130">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="fee00-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="fee00-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fee00-131">OUTPUTS</span></span>

### <span data-ttu-id="fee00-132">Microsoft. Azure. Management. RecoveryServices. Backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="fee00-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="fee00-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="fee00-133">NOTES</span></span>

## <span data-ttu-id="fee00-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fee00-134">RELATED LINKS</span></span>

[<span data-ttu-id="fee00-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="fee00-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="fee00-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="fee00-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


