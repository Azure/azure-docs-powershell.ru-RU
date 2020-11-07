---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
ms.openlocfilehash: 831bcdb76a0f24a2935f2ffd2ed0bf7df1c10042
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913872"
---
# <span data-ttu-id="39e3d-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="39e3d-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="39e3d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="39e3d-103">Восстановление удаленного ключа из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="39e3d-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39e3d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39e3d-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39e3d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39e3d-105">DESCRIPTION</span></span>
<span data-ttu-id="39e3d-106">Командлет **Undo-AzureKeyVaultKeyRemoval** восстановит ранее удаленную клавишу.</span><span class="sxs-lookup"><span data-stu-id="39e3d-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="39e3d-107">Восстановленный ключ будет активен и может использоваться для всех обычных операций с ключами.</span><span class="sxs-lookup"><span data-stu-id="39e3d-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="39e3d-108">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="39e3d-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="39e3d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39e3d-109">EXAMPLES</span></span>

### <span data-ttu-id="39e3d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="39e3d-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="39e3d-111">Эта команда восстанавливает в активном и рабочем состоянии раздел "MyKey", который был ранее удален.</span><span class="sxs-lookup"><span data-stu-id="39e3d-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="39e3d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39e3d-112">PARAMETERS</span></span>

### <span data-ttu-id="39e3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e3d-113">-DefaultProfile</span></span>
<span data-ttu-id="39e3d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="39e3d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39e3d-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="39e3d-115">-Name</span></span>
<span data-ttu-id="39e3d-116">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="39e3d-116">Key name.</span></span>
<span data-ttu-id="39e3d-117">Командлет создает полное доменное имя ключа из имени хранилища, выбранной в данный момент среды и имени ключа.</span><span class="sxs-lookup"><span data-stu-id="39e3d-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39e3d-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="39e3d-118">-VaultName</span></span>
<span data-ttu-id="39e3d-119">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="39e3d-119">Vault name.</span></span>
<span data-ttu-id="39e3d-120">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="39e3d-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39e3d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39e3d-121">-Confirm</span></span>
<span data-ttu-id="39e3d-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="39e3d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39e3d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39e3d-123">-WhatIf</span></span>
<span data-ttu-id="39e3d-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="39e3d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39e3d-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="39e3d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39e3d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e3d-126">CommonParameters</span></span>
<span data-ttu-id="39e3d-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39e3d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e3d-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39e3d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e3d-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39e3d-129">INPUTS</span></span>

### <span data-ttu-id="39e3d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="39e3d-130">System.String</span></span>

## <span data-ttu-id="39e3d-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39e3d-131">OUTPUTS</span></span>

### <span data-ttu-id="39e3d-132">Microsoft. Azure. Commands. KeyVault. Models. KeyBundle</span><span class="sxs-lookup"><span data-stu-id="39e3d-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="39e3d-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="39e3d-133">NOTES</span></span>

## <span data-ttu-id="39e3d-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39e3d-134">RELATED LINKS</span></span>

[<span data-ttu-id="39e3d-135">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="39e3d-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="39e3d-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="39e3d-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="39e3d-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="39e3d-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

