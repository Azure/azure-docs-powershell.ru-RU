---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: df29d88fbac1a8d2dc382522e24ff143cf075573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568746"
---
# <span data-ttu-id="b9730-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="b9730-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="b9730-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9730-102">SYNOPSIS</span></span>
<span data-ttu-id="b9730-103">Восстановление удаленного ключа из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b9730-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9730-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9730-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9730-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9730-105">DESCRIPTION</span></span>
<span data-ttu-id="b9730-106">Командлет **Undo-AzureKeyVaultKeyRemoval** восстановит ранее удаленную клавишу.</span><span class="sxs-lookup"><span data-stu-id="b9730-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="b9730-107">Восстановленный ключ будет активен и может использоваться для всех обычных операций с ключами.</span><span class="sxs-lookup"><span data-stu-id="b9730-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="b9730-108">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="b9730-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="b9730-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9730-109">EXAMPLES</span></span>

### <span data-ttu-id="b9730-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9730-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="b9730-111">Эта команда восстанавливает в активном и рабочем состоянии раздел "MyKey", который был ранее удален.</span><span class="sxs-lookup"><span data-stu-id="b9730-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="b9730-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9730-112">PARAMETERS</span></span>

### <span data-ttu-id="b9730-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b9730-113">-Name</span></span>
<span data-ttu-id="b9730-114">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="b9730-114">Key name.</span></span>
<span data-ttu-id="b9730-115">Командлет создает полное доменное имя ключа из имени хранилища, выбранной в данный момент среды и имени ключа.</span><span class="sxs-lookup"><span data-stu-id="b9730-115">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9730-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b9730-116">-VaultName</span></span>
<span data-ttu-id="b9730-117">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="b9730-117">Vault name.</span></span>
<span data-ttu-id="b9730-118">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="b9730-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9730-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9730-119">-Confirm</span></span>
<span data-ttu-id="b9730-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b9730-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9730-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9730-121">-WhatIf</span></span>
<span data-ttu-id="b9730-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b9730-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9730-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b9730-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9730-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9730-124">-DefaultProfile</span></span>
<span data-ttu-id="b9730-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9730-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9730-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9730-126">CommonParameters</span></span>
<span data-ttu-id="b9730-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9730-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9730-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9730-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9730-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9730-129">INPUTS</span></span>

### <span data-ttu-id="b9730-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b9730-130">System.String</span></span>

## <span data-ttu-id="b9730-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9730-131">OUTPUTS</span></span>

### <span data-ttu-id="b9730-132">Microsoft. Azure. Commands. KeyVault. Models. KeyBundle</span><span class="sxs-lookup"><span data-stu-id="b9730-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="b9730-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9730-133">NOTES</span></span>

## <span data-ttu-id="b9730-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9730-134">RELATED LINKS</span></span>

[<span data-ttu-id="b9730-135">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b9730-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="b9730-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b9730-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="b9730-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b9730-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

