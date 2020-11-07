---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 83737a7643c78ef4ec41d84e153690b3a53a8d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734449"
---
# <span data-ttu-id="e17a2-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="e17a2-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="e17a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e17a2-102">SYNOPSIS</span></span>
<span data-ttu-id="e17a2-103">Восстановление удаленного хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="e17a2-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e17a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e17a2-104">SYNTAX</span></span>

### <span data-ttu-id="e17a2-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e17a2-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e17a2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e17a2-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-ResourceGroupName] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e17a2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e17a2-107">DESCRIPTION</span></span>
<span data-ttu-id="e17a2-108">Командлет **Undo-AzureRmKeyVaultRemoval** восстановит ранее удаленное хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="e17a2-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="e17a2-109">Восстановленное хранилище станет активным после восстановления</span><span class="sxs-lookup"><span data-stu-id="e17a2-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="e17a2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e17a2-110">EXAMPLES</span></span>

### <span data-ttu-id="e17a2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e17a2-111">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="e17a2-112">Эта команда восстанавливает активное и пригодное состояние для хранилища ключей "MyKeyVault", который ранее был удален из группы ресурсов eastus2 Region и "MyResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="e17a2-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="e17a2-113">Он также заменяет Теги на новый тег.</span><span class="sxs-lookup"><span data-stu-id="e17a2-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="e17a2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e17a2-114">PARAMETERS</span></span>

### <span data-ttu-id="e17a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e17a2-115">-DefaultProfile</span></span>
<span data-ttu-id="e17a2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e17a2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e17a2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e17a2-117">-InputObject</span></span>
<span data-ttu-id="e17a2-118">Удален объект хранилища</span><span class="sxs-lookup"><span data-stu-id="e17a2-118">Deleted vault object</span></span>

```yaml
Type: PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e17a2-119">-Location</span><span class="sxs-lookup"><span data-stu-id="e17a2-119">-Location</span></span>
<span data-ttu-id="e17a2-120">Указывает исходный регион для удаленного хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e17a2-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e17a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="e17a2-122">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="e17a2-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17a2-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="e17a2-123">-Tag</span></span>
<span data-ttu-id="e17a2-124">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="e17a2-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e17a2-125">Например:</span><span class="sxs-lookup"><span data-stu-id="e17a2-125">For example:</span></span>

<span data-ttu-id="e17a2-126">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="e17a2-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17a2-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e17a2-127">-VaultName</span></span>
<span data-ttu-id="e17a2-128">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="e17a2-128">Vault name.</span></span>
<span data-ttu-id="e17a2-129">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="e17a2-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e17a2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e17a2-130">-Confirm</span></span>
<span data-ttu-id="e17a2-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e17a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e17a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e17a2-132">-WhatIf</span></span>
<span data-ttu-id="e17a2-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e17a2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e17a2-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e17a2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e17a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e17a2-135">CommonParameters</span></span>
<span data-ttu-id="e17a2-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e17a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e17a2-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e17a2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e17a2-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e17a2-138">INPUTS</span></span>

### <span data-ttu-id="e17a2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e17a2-139">System.String</span></span>
<span data-ttu-id="e17a2-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e17a2-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e17a2-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e17a2-141">OUTPUTS</span></span>

### <span data-ttu-id="e17a2-142">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e17a2-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="e17a2-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="e17a2-143">NOTES</span></span>

## <span data-ttu-id="e17a2-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e17a2-144">RELATED LINKS</span></span>

[<span data-ttu-id="e17a2-145">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e17a2-145">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="e17a2-146">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e17a2-146">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="e17a2-147">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e17a2-147">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
