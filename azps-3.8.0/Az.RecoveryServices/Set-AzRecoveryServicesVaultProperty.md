---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a9bd1eead98a7afb06e1f5b480f8a65fc5079bd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073521"
---
# <span data-ttu-id="85a65-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="85a65-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="85a65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85a65-102">SYNOPSIS</span></span>
<span data-ttu-id="85a65-103">Обновляет свойства хранилища.</span><span class="sxs-lookup"><span data-stu-id="85a65-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="85a65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85a65-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85a65-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85a65-105">DESCRIPTION</span></span>
<span data-ttu-id="85a65-106">Командлет **Set-AzRecoveryServicesVaultProperty** обновляет свойства хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="85a65-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="85a65-107">Вы можете использовать командлет **Set-AzRecoveryServicesVaultProperty** , чтобы получить доступ к текущим свойствам хранилища.</span><span class="sxs-lookup"><span data-stu-id="85a65-107">You can use **Set-AzRecoveryServicesVaultProperty** cmdlet to get the current properties of a vault.</span></span>
<span data-ttu-id="85a65-108">С помощью этого командлета **SoftDeleteFeatureState** свойство хранилища можно включить в любой момент.</span><span class="sxs-lookup"><span data-stu-id="85a65-108">Using this cmdlet **SoftDeleteFeatureState** property of a vault can be enabled at any point of time.</span></span>
<span data-ttu-id="85a65-109">Свойство **SoftDeleteFeatureState** хранилища можно отключить только в том случае, если в хранилище отсутствуют зарегистрированные контейнеры.</span><span class="sxs-lookup"><span data-stu-id="85a65-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>
<span data-ttu-id="85a65-110">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="85a65-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="85a65-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85a65-111">EXAMPLES</span></span>

### <span data-ttu-id="85a65-112">Пример 1: обновление SoftDeleteFeatureState хранилища</span><span class="sxs-lookup"><span data-stu-id="85a65-112">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="85a65-113">Первая команда получает объект хранилища и сохраняет его в переменной $vault.</span><span class="sxs-lookup"><span data-stu-id="85a65-113">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="85a65-114">Вторая команда обновляет свойство SoftDeleteFeatureState хранилища на состояние Enabled (включено).</span><span class="sxs-lookup"><span data-stu-id="85a65-114">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="85a65-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85a65-115">PARAMETERS</span></span>

### <span data-ttu-id="85a65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a65-116">-DefaultProfile</span></span>
<span data-ttu-id="85a65-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85a65-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85a65-118">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="85a65-118">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="85a65-119">SoftDeleteFeatureState хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="85a65-119">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="85a65-120">-VaultId</span><span class="sxs-lookup"><span data-stu-id="85a65-120">-VaultId</span></span>
<span data-ttu-id="85a65-121">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="85a65-121">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="85a65-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85a65-122">-Confirm</span></span>
<span data-ttu-id="85a65-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="85a65-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85a65-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a65-124">-WhatIf</span></span>
<span data-ttu-id="85a65-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="85a65-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85a65-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="85a65-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85a65-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a65-127">CommonParameters</span></span>
<span data-ttu-id="85a65-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85a65-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a65-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85a65-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a65-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85a65-130">INPUTS</span></span>

### <span data-ttu-id="85a65-131">System. String</span><span class="sxs-lookup"><span data-stu-id="85a65-131">System.String</span></span>

### <span data-ttu-id="85a65-132">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="85a65-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="85a65-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85a65-133">OUTPUTS</span></span>

### <span data-ttu-id="85a65-134">Microsoft. Azure. Management. RecoveryServices. Backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="85a65-134">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="85a65-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="85a65-135">NOTES</span></span>

## <span data-ttu-id="85a65-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85a65-136">RELATED LINKS</span></span>

[<span data-ttu-id="85a65-137">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="85a65-137">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="85a65-138">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="85a65-138">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


