---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://go.microsoft.com/fwlink/?LinkId=690160
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 28cd93fe9de14365e4de626729ec45a7aaa88cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569387"
---
# <span data-ttu-id="000c7-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="000c7-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="000c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="000c7-102">SYNOPSIS</span></span>
<span data-ttu-id="000c7-103">Создание хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="000c7-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="000c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="000c7-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="000c7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="000c7-105">DESCRIPTION</span></span>
<span data-ttu-id="000c7-106">Командлет **New-AzureRmKeyVault** создает хранилище ключей в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="000c7-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="000c7-107">Этот командлет также предоставляет пользователям разрешения на добавление, удаление или перечисление ключей и секретных параметров в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="000c7-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="000c7-108">Примечание. Если вы видите сообщение об ошибке **"не зарегистрирована подписка на использование пространства имен" Microsoft. KeyVault "** при попытке создания нового хранилища ключей, выполните команду **Register-AzureRmResourceProvider-ProviderNamespace" Microsoft. KeyVault "** , а затем снова запустите программу **New-AzureRmKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="000c7-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="000c7-109">Дополнительные сведения можно найти в разделе Register-AzureRmResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="000c7-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="000c7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="000c7-110">EXAMPLES</span></span>

### <span data-ttu-id="000c7-111">Пример 1: создание стандартного хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="000c7-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="000c7-112">Эта команда создает хранилище ключей с именем Contoso03Vault в Azure Region East США.</span><span class="sxs-lookup"><span data-stu-id="000c7-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="000c7-113">Команда добавляет хранилище ключей в группу ресурсов с именем Group14.</span><span class="sxs-lookup"><span data-stu-id="000c7-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="000c7-114">Поскольку в команде не указано значение параметра *SKU* , создается стандартное хранилище ключа.</span><span class="sxs-lookup"><span data-stu-id="000c7-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="000c7-115">Пример 2: создание хранилища ключей Premium</span><span class="sxs-lookup"><span data-stu-id="000c7-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="000c7-116">Эта команда создает хранилище ключей, как и в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="000c7-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="000c7-117">Тем не менее, он задает значение Premium для параметра *SKU* для создания хранилища ключей Premium.</span><span class="sxs-lookup"><span data-stu-id="000c7-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="000c7-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="000c7-118">PARAMETERS</span></span>

### <span data-ttu-id="000c7-119">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="000c7-119">-EnabledForDeployment</span></span>
<span data-ttu-id="000c7-120">Включает поставщик ресурсов Microsoft. COMPUTE для извлечения секретов из этого ключа, если это временное хранилище ссылается на создание ресурсов (например, при создании виртуальной машины).</span><span class="sxs-lookup"><span data-stu-id="000c7-120">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000c7-121">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="000c7-121">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="000c7-122">Позволяет службе шифрования дисков Azure получить секретные ключи и их перетекание из этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="000c7-122">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000c7-123">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="000c7-123">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="000c7-124">Позволяет диспетчеру ресурсов Azure получать секреты из этого хранилища ключей при ссылке на это хранилище ключей в развертывании шаблона.</span><span class="sxs-lookup"><span data-stu-id="000c7-124">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000c7-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="000c7-125">-EnableSoftDelete</span></span>
<span data-ttu-id="000c7-126">Если задано, для этого хранилища ключей включена функция "обратимого удаления".</span><span class="sxs-lookup"><span data-stu-id="000c7-126">If specified, 'soft delete' functionality is enabled for this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000c7-127">-Location</span><span class="sxs-lookup"><span data-stu-id="000c7-127">-Location</span></span>
<span data-ttu-id="000c7-128">Указывает область Azure, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="000c7-128">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="000c7-129">Используйте командную Get-AzureLocation ( https://msdn.microsoft.com/ Library/Azure/mt589064. aspx), чтобы просмотреть варианты выбора.</span><span class="sxs-lookup"><span data-stu-id="000c7-129">Use the command Get-AzureLocation (https://msdn.microsoft.com/ library/azure/mt589064.aspx) to see your choices.</span></span> <span data-ttu-id="000c7-130">Для получения дополнительных сведений введите `Get-Help Get-AzureLocation` .</span><span class="sxs-lookup"><span data-stu-id="000c7-130">For more information, type `Get-Help Get-AzureLocation`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000c7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="000c7-131">-ResourceGroupName</span></span>
<span data-ttu-id="000c7-132">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="000c7-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000c7-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="000c7-133">-Sku</span></span>
<span data-ttu-id="000c7-134">Указывает SKU экземпляра хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="000c7-134">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="000c7-135">Сведения о том, какие функции доступны для каждого SKU, можно найти на веб-сайте ценообразования для Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="000c7-135">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000c7-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="000c7-136">-Tag</span></span>
<span data-ttu-id="000c7-137">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="000c7-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="000c7-138">Например:</span><span class="sxs-lookup"><span data-stu-id="000c7-138">For example:</span></span>

<span data-ttu-id="000c7-139">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="000c7-139">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000c7-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="000c7-140">-VaultName</span></span>
<span data-ttu-id="000c7-141">Задает имя создаваемого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="000c7-141">Specifies the name of the key vault to create.</span></span> <span data-ttu-id="000c7-142">Имя может представлять собой любую комбинацию букв, цифр или дефисов.</span><span class="sxs-lookup"><span data-stu-id="000c7-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="000c7-143">Имя должно начинаться и заканчиваться на букву или цифру.</span><span class="sxs-lookup"><span data-stu-id="000c7-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="000c7-144">Имя должно быть универсальным уникальным.</span><span class="sxs-lookup"><span data-stu-id="000c7-144">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000c7-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="000c7-145">-Confirm</span></span>
<span data-ttu-id="000c7-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="000c7-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="000c7-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="000c7-147">-WhatIf</span></span>
<span data-ttu-id="000c7-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="000c7-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="000c7-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="000c7-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="000c7-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="000c7-150">-DefaultProfile</span></span>
<span data-ttu-id="000c7-151">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="000c7-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="000c7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="000c7-152">CommonParameters</span></span>
<span data-ttu-id="000c7-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="000c7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="000c7-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="000c7-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="000c7-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="000c7-155">INPUTS</span></span>

## <span data-ttu-id="000c7-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="000c7-156">OUTPUTS</span></span>

### <span data-ttu-id="000c7-157">Microsoft. Azure. Commands. KeyVault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="000c7-157">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="000c7-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="000c7-158">NOTES</span></span>

## <span data-ttu-id="000c7-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="000c7-159">RELATED LINKS</span></span>

[<span data-ttu-id="000c7-160">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="000c7-160">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="000c7-161">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="000c7-161">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
