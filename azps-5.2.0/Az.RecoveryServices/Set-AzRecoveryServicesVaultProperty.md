---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417223"
---
# <span data-ttu-id="ad1f8-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="ad1f8-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="ad1f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad1f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ad1f8-103">Обновляет свойства сейфа.</span><span class="sxs-lookup"><span data-stu-id="ad1f8-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="ad1f8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad1f8-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad1f8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad1f8-105">DESCRIPTION</span></span>
<span data-ttu-id="ad1f8-106">**Cmdlet Set-AzRecoveryServicesVaultProperty** обновляет свойства хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="ad1f8-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="ad1f8-107">Этот cmdlet возвращает обновленные свойства хранилища после текущей операции набора.</span><span class="sxs-lookup"><span data-stu-id="ad1f8-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="ad1f8-108">С помощью этого свойства cmdlet хранилища, например soft-delete, можно включить в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="ad1f8-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="ad1f8-109">**Свойство SoftDeleteFeatureState** хранилища можно отключить, только если в сейфе нет зарегистрированных контейнеров.</span><span class="sxs-lookup"><span data-stu-id="ad1f8-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="ad1f8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad1f8-110">EXAMPLES</span></span>

### <span data-ttu-id="ad1f8-111">Пример 1. Обновление статуса softDeleteFeature для сейфа</span><span class="sxs-lookup"><span data-stu-id="ad1f8-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="ad1f8-112">Первая команда получает объект Vault, а затем сохраняет его в $vault переменной.</span><span class="sxs-lookup"><span data-stu-id="ad1f8-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="ad1f8-113">Вторая команда обновляет свойство SoftDeleteFeatureState хранилища до состояния Enabled.</span><span class="sxs-lookup"><span data-stu-id="ad1f8-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="ad1f8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad1f8-114">PARAMETERS</span></span>

### <span data-ttu-id="ad1f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad1f8-115">-DefaultProfile</span></span>
<span data-ttu-id="ad1f8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad1f8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad1f8-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="ad1f8-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="ad1f8-118">SoftDeleteFeatureState хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="ad1f8-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ad1f8-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ad1f8-119">-VaultId</span></span>
<span data-ttu-id="ad1f8-120">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="ad1f8-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ad1f8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad1f8-121">-Confirm</span></span>
<span data-ttu-id="ad1f8-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad1f8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad1f8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad1f8-123">-WhatIf</span></span>
<span data-ttu-id="ad1f8-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad1f8-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="ad1f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad1f8-125">CommonParameters</span></span>
<span data-ttu-id="ad1f8-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad1f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad1f8-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad1f8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad1f8-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad1f8-128">INPUTS</span></span>

### <span data-ttu-id="ad1f8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ad1f8-129">System.String</span></span>

### <span data-ttu-id="ad1f8-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="ad1f8-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="ad1f8-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad1f8-131">OUTPUTS</span></span>

### <span data-ttu-id="ad1f8-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="ad1f8-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="ad1f8-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad1f8-133">NOTES</span></span>

## <span data-ttu-id="ad1f8-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad1f8-134">RELATED LINKS</span></span>

[<span data-ttu-id="ad1f8-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ad1f8-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="ad1f8-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="ad1f8-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


