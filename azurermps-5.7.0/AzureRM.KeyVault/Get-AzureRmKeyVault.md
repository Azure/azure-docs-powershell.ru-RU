---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 7b26eeb94854d21791bb662b4c1d9ce19973a193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569971"
---
# <span data-ttu-id="22a23-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="22a23-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="22a23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22a23-102">SYNOPSIS</span></span>
<span data-ttu-id="22a23-103">Получает ключевые хранилища.</span><span class="sxs-lookup"><span data-stu-id="22a23-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22a23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22a23-104">SYNTAX</span></span>

### <span data-ttu-id="22a23-105">ListAllVaultsInSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22a23-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22a23-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="22a23-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22a23-107">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="22a23-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22a23-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="22a23-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22a23-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22a23-109">DESCRIPTION</span></span>
<span data-ttu-id="22a23-110">Командлет **Get-AzureRmKeyVault** получает сведения о хранилищах ключей в подписке.</span><span class="sxs-lookup"><span data-stu-id="22a23-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="22a23-111">Вы можете просмотреть все экземпляры всех ключевых хранилищ в подписке или отфильтровать результаты по группе ресурсов или определенному хранилищу ключей.</span><span class="sxs-lookup"><span data-stu-id="22a23-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="22a23-112">Обратите внимание на то, что если задать группу ресурсов необязательно для этого командлета при получении единственного хранилища ключей, необходимо сделать это для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="22a23-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="22a23-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22a23-113">EXAMPLES</span></span>

### <span data-ttu-id="22a23-114">Пример 1: получение всех ключевых хранилищ в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="22a23-114">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="22a23-115">Эта команда получает все ключевые хранилища в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="22a23-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="22a23-116">Пример 2: получение определенного ключевого хранилища</span><span class="sxs-lookup"><span data-stu-id="22a23-116">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="22a23-117">Эта команда получает хранилище ключей с именем Contoso03Vault в текущей подписке, а затем сохраняет его в переменной $MyVault.</span><span class="sxs-lookup"><span data-stu-id="22a23-117">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="22a23-118">Вы можете узнать о свойствах $MyVault, чтобы получить подробные сведения о хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="22a23-118">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="22a23-119">Пример 3: Получение хранилища ключей в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="22a23-119">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="22a23-120">Эта команда возвращает все хранилища ключей в группе ресурсов с именем ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="22a23-120">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="22a23-121">Пример 4: получение всех удаленных хранилищ ключей в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="22a23-121">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="22a23-122">Эта команда получает все удаленные хранилища ключей в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="22a23-122">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="22a23-123">Пример 5: получение удаленного хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="22a23-123">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="22a23-124">Эта команда получает удаленные сведения о хранилище ключей с именем Contoso03Vault в текущей подписке и в eastus2 регионе.</span><span class="sxs-lookup"><span data-stu-id="22a23-124">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="22a23-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22a23-125">PARAMETERS</span></span>

### <span data-ttu-id="22a23-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a23-126">-DefaultProfile</span></span>
<span data-ttu-id="22a23-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="22a23-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22a23-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="22a23-128">-InRemovedState</span></span>
<span data-ttu-id="22a23-129">Указывает, нужно ли отображать ранее удаленные хранилища в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="22a23-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a23-130">-Location</span><span class="sxs-lookup"><span data-stu-id="22a23-130">-Location</span></span>
<span data-ttu-id="22a23-131">Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="22a23-131">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a23-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a23-132">-ResourceGroupName</span></span>
<span data-ttu-id="22a23-133">Указывает имя группы ресурсов, связанной с запрашиваемым хранилищем ключей или хранилищами ключей.</span><span class="sxs-lookup"><span data-stu-id="22a23-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a23-134">-Тег</span><span class="sxs-lookup"><span data-stu-id="22a23-134">-Tag</span></span>
<span data-ttu-id="22a23-135">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="22a23-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="22a23-136">Например:</span><span class="sxs-lookup"><span data-stu-id="22a23-136">For example:</span></span>

<span data-ttu-id="22a23-137">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="22a23-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a23-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="22a23-138">-VaultName</span></span>
<span data-ttu-id="22a23-139">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="22a23-139">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a23-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a23-140">CommonParameters</span></span>
<span data-ttu-id="22a23-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22a23-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a23-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22a23-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a23-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22a23-143">INPUTS</span></span>

### <span data-ttu-id="22a23-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="22a23-144">None</span></span>
<span data-ttu-id="22a23-145">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="22a23-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22a23-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22a23-146">OUTPUTS</span></span>

### <span data-ttu-id="22a23-147">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="22a23-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="22a23-148">System. Collections. Generic. List ' 1 [Microsoft. Azure. PSKeyVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="22a23-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem]</span></span>

### <span data-ttu-id="22a23-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="22a23-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

### <span data-ttu-id="22a23-150">System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span><span class="sxs-lookup"><span data-stu-id="22a23-150">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span></span>

## <span data-ttu-id="22a23-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="22a23-151">NOTES</span></span>

## <span data-ttu-id="22a23-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22a23-152">RELATED LINKS</span></span>

[<span data-ttu-id="22a23-153">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="22a23-153">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="22a23-154">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="22a23-154">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
