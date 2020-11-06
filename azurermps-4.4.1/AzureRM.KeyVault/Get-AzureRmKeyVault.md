---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://go.microsoft.com/fwlink/?LinkID=690161
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 9a4d3399dd19d7dfced4f695623eef2fe0dba29d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559783"
---
# <span data-ttu-id="8a467-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="8a467-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="8a467-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a467-102">SYNOPSIS</span></span>
<span data-ttu-id="8a467-103">Получает ключевые хранилища.</span><span class="sxs-lookup"><span data-stu-id="8a467-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a467-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a467-104">SYNTAX</span></span>

### <span data-ttu-id="8a467-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="8a467-105">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a467-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="8a467-106">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a467-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8a467-107">ListVaultsByResourceGroup</span></span>
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a467-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="8a467-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a467-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="8a467-109">ListAllVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a467-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a467-110">DESCRIPTION</span></span>
<span data-ttu-id="8a467-111">Командлет **Get-AzureRmKeyVault** получает сведения о хранилищах ключей в подписке.</span><span class="sxs-lookup"><span data-stu-id="8a467-111">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="8a467-112">Вы можете просмотреть все экземпляры всех ключевых хранилищ в подписке или отфильтровать результаты по группе ресурсов или определенному хранилищу ключей.</span><span class="sxs-lookup"><span data-stu-id="8a467-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="8a467-113">Обратите внимание на то, что если задать группу ресурсов необязательно для этого командлета при получении единственного хранилища ключей, необходимо сделать это для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="8a467-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="8a467-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a467-114">EXAMPLES</span></span>

### <span data-ttu-id="8a467-115">Пример 1: получение всех ключевых хранилищ в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="8a467-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="8a467-116">Эта команда получает все ключевые хранилища в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="8a467-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="8a467-117">Пример 2: получение определенного ключевого хранилища</span><span class="sxs-lookup"><span data-stu-id="8a467-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="8a467-118">Эта команда получает хранилище ключей с именем Contoso03Vault в текущей подписке, а затем сохраняет его в переменной $MyVault.</span><span class="sxs-lookup"><span data-stu-id="8a467-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="8a467-119">Вы можете узнать о свойствах $MyVault, чтобы получить подробные сведения о хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="8a467-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="8a467-120">Пример 3: Получение хранилища ключей в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="8a467-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="8a467-121">Эта команда возвращает все хранилища ключей в группе ресурсов с именем ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8a467-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="8a467-122">Пример 4: получение всех удаленных хранилищ ключей в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="8a467-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="8a467-123">Эта команда получает все удаленные хранилища ключей в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="8a467-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="8a467-124">Пример 5: получение удаленного хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="8a467-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="8a467-125">Эта команда получает удаленные сведения о хранилище ключей с именем Contoso03Vault в текущей подписке и в eastus2 регионе.</span><span class="sxs-lookup"><span data-stu-id="8a467-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="8a467-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a467-126">PARAMETERS</span></span>

### <span data-ttu-id="8a467-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="8a467-127">-InRemovedState</span></span>
<span data-ttu-id="8a467-128">Указывает, нужно ли отображать ранее удаленные хранилища в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8a467-128">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a467-129">-Location</span><span class="sxs-lookup"><span data-stu-id="8a467-129">-Location</span></span>
<span data-ttu-id="8a467-130">Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="8a467-130">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a467-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a467-131">-ResourceGroupName</span></span>
<span data-ttu-id="8a467-132">Указывает имя группы ресурсов, связанной с запрашиваемым хранилищем ключей или хранилищами ключей.</span><span class="sxs-lookup"><span data-stu-id="8a467-132">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a467-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="8a467-133">-Tag</span></span>
<span data-ttu-id="8a467-134">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="8a467-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8a467-135">Например:</span><span class="sxs-lookup"><span data-stu-id="8a467-135">For example:</span></span>

<span data-ttu-id="8a467-136">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8a467-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a467-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8a467-137">-VaultName</span></span>
<span data-ttu-id="8a467-138">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8a467-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a467-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a467-139">-DefaultProfile</span></span>
<span data-ttu-id="8a467-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a467-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a467-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a467-141">CommonParameters</span></span>
<span data-ttu-id="8a467-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a467-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a467-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a467-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a467-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a467-144">INPUTS</span></span>

## <span data-ttu-id="8a467-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a467-145">OUTPUTS</span></span>

### <span data-ttu-id="8a467-146">Microsoft. Azure. Commands. KeyVault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="8a467-146">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="8a467-147">System. Collections. Generic. List ' 1 [Microsoft. Azure. PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="8a467-147">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="8a467-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="8a467-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="8a467-149">System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="8a467-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="8a467-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a467-150">NOTES</span></span>

## <span data-ttu-id="8a467-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a467-151">RELATED LINKS</span></span>

[<span data-ttu-id="8a467-152">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="8a467-152">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="8a467-153">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="8a467-153">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
