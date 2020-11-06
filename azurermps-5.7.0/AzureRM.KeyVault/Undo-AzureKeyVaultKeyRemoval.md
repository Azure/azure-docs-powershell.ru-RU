---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: 29a7c2d3bb2060b77871cea0c088c50a59197cb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559044"
---
# <span data-ttu-id="fe445-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="fe445-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="fe445-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe445-102">SYNOPSIS</span></span>
<span data-ttu-id="fe445-103">Восстановление удаленного ключа из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="fe445-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe445-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe445-104">SYNTAX</span></span>

### <span data-ttu-id="fe445-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe445-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe445-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fe445-106">InputObject</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe445-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe445-107">DESCRIPTION</span></span>
<span data-ttu-id="fe445-108">Командлет **Undo-AzureKeyVaultKeyRemoval** восстановит ранее удаленную клавишу.</span><span class="sxs-lookup"><span data-stu-id="fe445-108">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="fe445-109">Восстановленный ключ будет активен и может использоваться для всех обычных операций с ключами.</span><span class="sxs-lookup"><span data-stu-id="fe445-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="fe445-110">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="fe445-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="fe445-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe445-111">EXAMPLES</span></span>

### <span data-ttu-id="fe445-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe445-112">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="fe445-113">Эта команда восстанавливает в активном и рабочем состоянии раздел "MyKey", который был ранее удален.</span><span class="sxs-lookup"><span data-stu-id="fe445-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="fe445-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe445-114">PARAMETERS</span></span>

### <span data-ttu-id="fe445-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe445-115">-DefaultProfile</span></span>
<span data-ttu-id="fe445-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fe445-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe445-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe445-117">-InputObject</span></span>
<span data-ttu-id="fe445-118">Удаленный объект Key</span><span class="sxs-lookup"><span data-stu-id="fe445-118">Deleted key object</span></span>

```yaml
Type: PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe445-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fe445-119">-Name</span></span>
<span data-ttu-id="fe445-120">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="fe445-120">Key name.</span></span>
<span data-ttu-id="fe445-121">Командлет создает полное доменное имя ключа из имени хранилища, выбранной в данный момент среды и имени ключа.</span><span class="sxs-lookup"><span data-stu-id="fe445-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe445-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fe445-122">-VaultName</span></span>
<span data-ttu-id="fe445-123">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="fe445-123">Vault name.</span></span>
<span data-ttu-id="fe445-124">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="fe445-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe445-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe445-125">-Confirm</span></span>
<span data-ttu-id="fe445-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe445-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe445-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe445-127">-WhatIf</span></span>
<span data-ttu-id="fe445-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe445-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe445-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe445-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe445-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe445-130">CommonParameters</span></span>
<span data-ttu-id="fe445-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe445-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe445-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe445-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe445-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe445-133">INPUTS</span></span>

### <span data-ttu-id="fe445-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fe445-134">System.String</span></span>

## <span data-ttu-id="fe445-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe445-135">OUTPUTS</span></span>

### <span data-ttu-id="fe445-136">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fe445-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="fe445-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe445-137">NOTES</span></span>

## <span data-ttu-id="fe445-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe445-138">RELATED LINKS</span></span>

[<span data-ttu-id="fe445-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fe445-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="fe445-140">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fe445-140">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="fe445-141">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fe445-141">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

