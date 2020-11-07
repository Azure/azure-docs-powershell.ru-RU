---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: 5b0e67fbbead536803dba8efeb2c8a61d7f75c5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911149"
---
# <span data-ttu-id="2962b-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="2962b-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="2962b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2962b-102">SYNOPSIS</span></span>
<span data-ttu-id="2962b-103">Восстановление удаленного ключа из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="2962b-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="2962b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2962b-104">SYNTAX</span></span>

```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2962b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2962b-105">DESCRIPTION</span></span>
<span data-ttu-id="2962b-106">Командлет **Undo-AzKeyVaultKeyRemoval** восстановит ранее удаленную клавишу.</span><span class="sxs-lookup"><span data-stu-id="2962b-106">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="2962b-107">Восстановленный ключ будет активен и может использоваться для всех обычных операций с ключами.</span><span class="sxs-lookup"><span data-stu-id="2962b-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="2962b-108">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="2962b-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="2962b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2962b-109">EXAMPLES</span></span>

### <span data-ttu-id="2962b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2962b-110">Example 1</span></span>
```
PS C:\>Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="2962b-111">Эта команда восстанавливает в активном и рабочем состоянии раздел "MyKey", который был ранее удален.</span><span class="sxs-lookup"><span data-stu-id="2962b-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="2962b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2962b-112">PARAMETERS</span></span>

### <span data-ttu-id="2962b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2962b-113">-DefaultProfile</span></span>
<span data-ttu-id="2962b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2962b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2962b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2962b-115">-Name</span></span>
<span data-ttu-id="2962b-116">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="2962b-116">Key name.</span></span>
<span data-ttu-id="2962b-117">Командлет создает полное доменное имя ключа из имени хранилища, выбранной в данный момент среды и имени ключа.</span><span class="sxs-lookup"><span data-stu-id="2962b-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="2962b-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2962b-118">-VaultName</span></span>
<span data-ttu-id="2962b-119">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="2962b-119">Vault name.</span></span>
<span data-ttu-id="2962b-120">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="2962b-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2962b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2962b-121">-Confirm</span></span>
<span data-ttu-id="2962b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2962b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2962b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2962b-123">-WhatIf</span></span>
<span data-ttu-id="2962b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2962b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2962b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2962b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2962b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2962b-126">CommonParameters</span></span>
<span data-ttu-id="2962b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2962b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2962b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2962b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2962b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2962b-129">INPUTS</span></span>

### <span data-ttu-id="2962b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2962b-130">System.String</span></span>

## <span data-ttu-id="2962b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2962b-131">OUTPUTS</span></span>

### <span data-ttu-id="2962b-132">Microsoft. Azure. Commands. KeyVault. Models. KeyBundle</span><span class="sxs-lookup"><span data-stu-id="2962b-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="2962b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="2962b-133">NOTES</span></span>

## <span data-ttu-id="2962b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2962b-134">RELATED LINKS</span></span>

[<span data-ttu-id="2962b-135">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2962b-135">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="2962b-136">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2962b-136">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="2962b-137">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2962b-137">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

