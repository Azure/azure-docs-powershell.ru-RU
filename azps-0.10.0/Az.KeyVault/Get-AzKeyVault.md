---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: aaace602cd50f9464021b1dcbefe39272e1621bb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910308"
---
# <span data-ttu-id="08d38-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="08d38-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="08d38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08d38-102">SYNOPSIS</span></span>
<span data-ttu-id="08d38-103">Получает ключевые хранилища.</span><span class="sxs-lookup"><span data-stu-id="08d38-103">Gets key vaults.</span></span>

## <span data-ttu-id="08d38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08d38-104">SYNTAX</span></span>

### <span data-ttu-id="08d38-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="08d38-105">GetVaultByName</span></span>
```
Get-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08d38-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="08d38-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08d38-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="08d38-107">ListVaultsByResourceGroup</span></span>
```
Get-AzKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08d38-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="08d38-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08d38-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="08d38-109">ListAllVaultsInSubscription</span></span>
```
Get-AzKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08d38-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08d38-110">DESCRIPTION</span></span>
<span data-ttu-id="08d38-111">Командлет **Get-AzKeyVault** получает сведения о хранилищах ключей в подписке.</span><span class="sxs-lookup"><span data-stu-id="08d38-111">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="08d38-112">Вы можете просмотреть все экземпляры всех ключевых хранилищ в подписке или отфильтровать результаты по группе ресурсов или определенному хранилищу ключей.</span><span class="sxs-lookup"><span data-stu-id="08d38-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="08d38-113">Обратите внимание на то, что если задать группу ресурсов необязательно для этого командлета при получении единственного хранилища ключей, необходимо сделать это для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="08d38-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="08d38-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08d38-114">EXAMPLES</span></span>

### <span data-ttu-id="08d38-115">Пример 1: получение всех ключевых хранилищ в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="08d38-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzKeyVault
```

<span data-ttu-id="08d38-116">Эта команда получает все ключевые хранилища в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="08d38-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="08d38-117">Пример 2: получение определенного ключевого хранилища</span><span class="sxs-lookup"><span data-stu-id="08d38-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="08d38-118">Эта команда получает хранилище ключей с именем Contoso03Vault в текущей подписке, а затем сохраняет его в переменной $MyVault.</span><span class="sxs-lookup"><span data-stu-id="08d38-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="08d38-119">Вы можете узнать о свойствах $MyVault, чтобы получить подробные сведения о хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="08d38-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="08d38-120">Пример 3: Получение хранилища ключей в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="08d38-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="08d38-121">Эта команда возвращает все хранилища ключей в группе ресурсов с именем ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="08d38-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="08d38-122">Пример 4: получение всех удаленных хранилищ ключей в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="08d38-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzKeyVault -InRemovedState
```

<span data-ttu-id="08d38-123">Эта команда получает все удаленные хранилища ключей в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="08d38-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="08d38-124">Пример 5: получение удаленного хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="08d38-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="08d38-125">Эта команда получает удаленные сведения о хранилище ключей с именем Contoso03Vault в текущей подписке и в eastus2 регионе.</span><span class="sxs-lookup"><span data-stu-id="08d38-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="08d38-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08d38-126">PARAMETERS</span></span>

### <span data-ttu-id="08d38-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08d38-127">-DefaultProfile</span></span>
<span data-ttu-id="08d38-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="08d38-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08d38-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="08d38-129">-InRemovedState</span></span>
<span data-ttu-id="08d38-130">Указывает, нужно ли отображать ранее удаленные хранилища в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="08d38-130">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="08d38-131">-Location</span><span class="sxs-lookup"><span data-stu-id="08d38-131">-Location</span></span>
<span data-ttu-id="08d38-132">Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="08d38-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08d38-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08d38-133">-ResourceGroupName</span></span>
<span data-ttu-id="08d38-134">Указывает имя группы ресурсов, связанной с запрашиваемым хранилищем ключей или хранилищами ключей.</span><span class="sxs-lookup"><span data-stu-id="08d38-134">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08d38-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="08d38-135">-Tag</span></span>
<span data-ttu-id="08d38-136">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="08d38-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="08d38-137">Например:</span><span class="sxs-lookup"><span data-stu-id="08d38-137">For example:</span></span>

<span data-ttu-id="08d38-138">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="08d38-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="08d38-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="08d38-139">-VaultName</span></span>
<span data-ttu-id="08d38-140">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="08d38-140">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08d38-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08d38-141">CommonParameters</span></span>
<span data-ttu-id="08d38-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08d38-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08d38-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08d38-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08d38-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08d38-144">INPUTS</span></span>

### <span data-ttu-id="08d38-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="08d38-145">None</span></span>
<span data-ttu-id="08d38-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="08d38-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="08d38-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08d38-147">OUTPUTS</span></span>

### <span data-ttu-id="08d38-148">Microsoft. Azure. Commands. KeyVault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="08d38-148">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="08d38-149">System. Collections. Generic. List ' 1 [Microsoft. Azure. PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="08d38-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="08d38-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="08d38-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="08d38-151">System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="08d38-151">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="08d38-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="08d38-152">NOTES</span></span>

## <span data-ttu-id="08d38-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08d38-153">RELATED LINKS</span></span>

[<span data-ttu-id="08d38-154">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="08d38-154">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="08d38-155">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="08d38-155">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
