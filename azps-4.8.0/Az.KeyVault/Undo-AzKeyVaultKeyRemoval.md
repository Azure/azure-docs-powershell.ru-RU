---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: c2b4fec2524ed3ddac62cf687af33ba3f76f13e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079972"
---
# <span data-ttu-id="114a5-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="114a5-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="114a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="114a5-102">SYNOPSIS</span></span>
<span data-ttu-id="114a5-103">Восстановление удаленного ключа из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="114a5-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="114a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="114a5-104">SYNTAX</span></span>

### <span data-ttu-id="114a5-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="114a5-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="114a5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="114a5-106">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="114a5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="114a5-107">DESCRIPTION</span></span>
<span data-ttu-id="114a5-108">Командлет **Undo-AzKeyVaultKeyRemoval** восстановит ранее удаленную клавишу.</span><span class="sxs-lookup"><span data-stu-id="114a5-108">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="114a5-109">Восстановленный ключ будет активен и может использоваться для всех обычных операций с ключами.</span><span class="sxs-lookup"><span data-stu-id="114a5-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="114a5-110">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="114a5-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="114a5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="114a5-111">EXAMPLES</span></span>

### <span data-ttu-id="114a5-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="114a5-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="114a5-113">Эта команда восстанавливает в активном и рабочем состоянии раздел "MyKey", который был ранее удален.</span><span class="sxs-lookup"><span data-stu-id="114a5-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="114a5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="114a5-114">PARAMETERS</span></span>

### <span data-ttu-id="114a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="114a5-115">-DefaultProfile</span></span>
<span data-ttu-id="114a5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="114a5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="114a5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="114a5-117">-InputObject</span></span>
<span data-ttu-id="114a5-118">Удаленный объект Key</span><span class="sxs-lookup"><span data-stu-id="114a5-118">Deleted key object</span></span>

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

### <span data-ttu-id="114a5-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="114a5-119">-Name</span></span>
<span data-ttu-id="114a5-120">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="114a5-120">Key name.</span></span>
<span data-ttu-id="114a5-121">Командлет создает полное доменное имя ключа из имени хранилища, выбранной в данный момент среды и имени ключа.</span><span class="sxs-lookup"><span data-stu-id="114a5-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="114a5-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="114a5-122">-VaultName</span></span>
<span data-ttu-id="114a5-123">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="114a5-123">Vault name.</span></span>
<span data-ttu-id="114a5-124">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="114a5-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="114a5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="114a5-125">-Confirm</span></span>
<span data-ttu-id="114a5-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="114a5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="114a5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="114a5-127">-WhatIf</span></span>
<span data-ttu-id="114a5-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="114a5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="114a5-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="114a5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="114a5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114a5-130">CommonParameters</span></span>
<span data-ttu-id="114a5-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="114a5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114a5-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="114a5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114a5-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="114a5-133">INPUTS</span></span>

### <span data-ttu-id="114a5-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="114a5-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="114a5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="114a5-135">OUTPUTS</span></span>

### <span data-ttu-id="114a5-136">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="114a5-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="114a5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="114a5-137">NOTES</span></span>

## <span data-ttu-id="114a5-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="114a5-138">RELATED LINKS</span></span>

[<span data-ttu-id="114a5-139">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="114a5-139">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="114a5-140">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="114a5-140">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="114a5-141">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="114a5-141">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)
