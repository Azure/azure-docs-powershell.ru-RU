---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azmanagedhsmkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
ms.openlocfilehash: be1713584a1d0ce897c1c728f6aa7ae8b6ca3255
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245280"
---
# <span data-ttu-id="792e2-101">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="792e2-101">Undo-AzManagedHsmKeyRemoval</span></span>

## <span data-ttu-id="792e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="792e2-102">SYNOPSIS</span></span>
<span data-ttu-id="792e2-103">Восстановление удаленного ключа из управляемого HSM-аппарата в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="792e2-103">Recovers a deleted key in a managed HSM into an active state.</span></span>

## <span data-ttu-id="792e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="792e2-104">SYNTAX</span></span>

### <span data-ttu-id="792e2-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="792e2-105">Default (Default)</span></span>
```
Undo-AzManagedHsmKeyRemoval [-HsmName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="792e2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="792e2-106">InputObject</span></span>
```
Undo-AzManagedHsmKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="792e2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="792e2-107">DESCRIPTION</span></span>
<span data-ttu-id="792e2-108">Командлет **Undo-AzManagedHsmKeyRemoval** восстановит ранее удаленную клавишу.</span><span class="sxs-lookup"><span data-stu-id="792e2-108">The **Undo-AzManagedHsmKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="792e2-109">Восстановленный ключ будет активен и может использоваться для всех обычных операций с ключами.</span><span class="sxs-lookup"><span data-stu-id="792e2-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="792e2-110">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="792e2-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="792e2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="792e2-111">EXAMPLES</span></span>

### <span data-ttu-id="792e2-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="792e2-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzManagedHsmKeyRemoval -HsmName testmhsm -Name testkey001

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="792e2-113">Эта команда восстанавливает в активном и рабочем состоянии раздел "testkey001", который был ранее удален.</span><span class="sxs-lookup"><span data-stu-id="792e2-113">This command will recover the key 'testkey001' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="792e2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="792e2-114">PARAMETERS</span></span>

### <span data-ttu-id="792e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792e2-115">-DefaultProfile</span></span>
<span data-ttu-id="792e2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="792e2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="792e2-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="792e2-117">-HsmName</span></span>
<span data-ttu-id="792e2-118">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="792e2-118">HSM name.</span></span> <span data-ttu-id="792e2-119">Командлет создает полное доменное имя управляемого HSM-файла на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="792e2-119">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792e2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="792e2-120">-InputObject</span></span>
<span data-ttu-id="792e2-121">Удаленный объект Key</span><span class="sxs-lookup"><span data-stu-id="792e2-121">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="792e2-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="792e2-122">-Name</span></span>
<span data-ttu-id="792e2-123">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="792e2-123">Key name.</span></span>
<span data-ttu-id="792e2-124">Командлет конструирует полное доменное имя ключа из управляемого имени HSM, в настоящее время выбранной среды и имени ключа.</span><span class="sxs-lookup"><span data-stu-id="792e2-124">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792e2-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="792e2-125">-Confirm</span></span>
<span data-ttu-id="792e2-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="792e2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="792e2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="792e2-127">-WhatIf</span></span>
<span data-ttu-id="792e2-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="792e2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="792e2-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="792e2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="792e2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792e2-130">CommonParameters</span></span>
<span data-ttu-id="792e2-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="792e2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792e2-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="792e2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792e2-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="792e2-133">INPUTS</span></span>

### <span data-ttu-id="792e2-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="792e2-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="792e2-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="792e2-135">OUTPUTS</span></span>

### <span data-ttu-id="792e2-136">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="792e2-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="792e2-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="792e2-137">NOTES</span></span>

## <span data-ttu-id="792e2-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="792e2-138">RELATED LINKS</span></span>

[<span data-ttu-id="792e2-139">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="792e2-139">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="792e2-140">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="792e2-140">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="792e2-141">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="792e2-141">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="792e2-142">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="792e2-142">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)

[<span data-ttu-id="792e2-143">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="792e2-143">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="792e2-144">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="792e2-144">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)