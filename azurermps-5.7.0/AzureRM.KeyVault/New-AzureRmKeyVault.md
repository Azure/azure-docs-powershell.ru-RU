---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 7cc4af3e849a6cd24c2144c6e92c990da261e9d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734023"
---
# <span data-ttu-id="2ca8e-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="2ca8e-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="2ca8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ca8e-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca8e-103">Создание хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ca8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ca8e-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca8e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ca8e-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca8e-106">Командлет **New-AzureRmKeyVault** создает хранилище ключей в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="2ca8e-107">Этот командлет также предоставляет пользователям разрешения на добавление, удаление или перечисление ключей и секретных параметров в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="2ca8e-108">Примечание. Если вы видите сообщение об ошибке **"не зарегистрирована подписка на использование пространства имен" Microsoft. KeyVault "** при попытке создания нового хранилища ключей, выполните команду **Register-AzureRmResourceProvider-ProviderNamespace" Microsoft. KeyVault "** , а затем снова запустите программу **New-AzureRmKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="2ca8e-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="2ca8e-109">Дополнительные сведения можно найти в разделе Register-AzureRmResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="2ca8e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ca8e-110">EXAMPLES</span></span>

### <span data-ttu-id="2ca8e-111">Пример 1: создание стандартного хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="2ca8e-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="2ca8e-112">Эта команда создает хранилище ключей с именем Contoso03Vault в Azure Region East США.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="2ca8e-113">Команда добавляет хранилище ключей в группу ресурсов с именем Group14.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="2ca8e-114">Поскольку в команде не указано значение параметра *SKU* , создается стандартное хранилище ключа.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="2ca8e-115">Пример 2: создание хранилища ключей Premium</span><span class="sxs-lookup"><span data-stu-id="2ca8e-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="2ca8e-116">Эта команда создает хранилище ключей, как и в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="2ca8e-117">Тем не менее, он задает значение Premium для параметра *SKU* для создания хранилища ключей Premium.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="2ca8e-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ca8e-118">PARAMETERS</span></span>

### <span data-ttu-id="2ca8e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca8e-119">-DefaultProfile</span></span>
<span data-ttu-id="2ca8e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2ca8e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ca8e-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="2ca8e-121">-EnabledForDeployment</span></span>
<span data-ttu-id="2ca8e-122">Включает поставщик ресурсов Microsoft. COMPUTE для извлечения секретов из этого ключа, если это временное хранилище ссылается на создание ресурсов (например, при создании виртуальной машины).</span><span class="sxs-lookup"><span data-stu-id="2ca8e-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca8e-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="2ca8e-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="2ca8e-124">Позволяет службе шифрования дисков Azure получить секретные ключи и их перетекание из этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca8e-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="2ca8e-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="2ca8e-126">Позволяет диспетчеру ресурсов Azure получать секреты из этого хранилища ключей при ссылке на это хранилище ключей в развертывании шаблона.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca8e-127">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="2ca8e-127">-EnableSoftDelete</span></span>
<span data-ttu-id="2ca8e-128">Указывает, что функция мягкого удаления включена для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-128">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="2ca8e-129">Если включено мягкое удаление, в течение льготного периода вы можете восстановить это хранилище ключей и его содержимое после удаления.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-129">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>

<span data-ttu-id="2ca8e-130">Дополнительные сведения об этой функции можно найти в разделе Общие сведения о [мягком удалении для хранилища ключей Azure](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span><span class="sxs-lookup"><span data-stu-id="2ca8e-130">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="2ca8e-131">Инструкции — Узнайте, [как использовать ключевое руководство с мягким удалением с помощью PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span><span class="sxs-lookup"><span data-stu-id="2ca8e-131">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca8e-132">-Location</span><span class="sxs-lookup"><span data-stu-id="2ca8e-132">-Location</span></span>
<span data-ttu-id="2ca8e-133">Указывает область Azure, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-133">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="2ca8e-134">С помощью команды [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) можно просмотреть варианты выбора.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-134">Use the command [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) to see your choices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca8e-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ca8e-135">-Name</span></span>
<span data-ttu-id="2ca8e-136">Задает имя создаваемого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-136">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="2ca8e-137">Имя может представлять собой любую комбинацию букв, цифр или дефисов.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-137">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="2ca8e-138">Имя должно начинаться и заканчиваться на букву или цифру.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-138">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="2ca8e-139">Имя должно быть универсальным уникальным.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-139">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca8e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca8e-140">-ResourceGroupName</span></span>
<span data-ttu-id="2ca8e-141">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-141">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="2ca8e-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="2ca8e-142">-Sku</span></span>
<span data-ttu-id="2ca8e-143">Указывает SKU экземпляра хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-143">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="2ca8e-144">Сведения о том, какие функции доступны для каждого SKU, можно найти на веб-сайте ценообразования для Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="2ca8e-144">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca8e-145">-Тег</span><span class="sxs-lookup"><span data-stu-id="2ca8e-145">-Tag</span></span>
<span data-ttu-id="2ca8e-146">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-146">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2ca8e-147">Например:</span><span class="sxs-lookup"><span data-stu-id="2ca8e-147">For example:</span></span>

<span data-ttu-id="2ca8e-148">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2ca8e-148">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca8e-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ca8e-149">-Confirm</span></span>
<span data-ttu-id="2ca8e-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ca8e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca8e-151">-WhatIf</span></span>
<span data-ttu-id="2ca8e-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ca8e-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ca8e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca8e-154">CommonParameters</span></span>
<span data-ttu-id="2ca8e-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca8e-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca8e-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca8e-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ca8e-157">INPUTS</span></span>

### <span data-ttu-id="2ca8e-158">Ничего</span><span class="sxs-lookup"><span data-stu-id="2ca8e-158">None</span></span>
<span data-ttu-id="2ca8e-159">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2ca8e-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2ca8e-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ca8e-160">OUTPUTS</span></span>

### <span data-ttu-id="2ca8e-161">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="2ca8e-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="2ca8e-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ca8e-162">NOTES</span></span>

## <span data-ttu-id="2ca8e-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ca8e-163">RELATED LINKS</span></span>

[<span data-ttu-id="2ca8e-164">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="2ca8e-164">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="2ca8e-165">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="2ca8e-165">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
