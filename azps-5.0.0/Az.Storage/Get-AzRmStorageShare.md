---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 90edd254eb77b03f4f4d26761020d71025960426
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249761"
---
# <span data-ttu-id="0d575-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0d575-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="0d575-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d575-102">SYNOPSIS</span></span>
<span data-ttu-id="0d575-103">Возвращает или отображает общие файлы хранилища.</span><span class="sxs-lookup"><span data-stu-id="0d575-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="0d575-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d575-104">SYNTAX</span></span>

### <span data-ttu-id="0d575-105">AccountNameSingle (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d575-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d575-106">Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="0d575-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d575-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="0d575-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d575-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0d575-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d575-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="0d575-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d575-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d575-110">DESCRIPTION</span></span>
<span data-ttu-id="0d575-111">Командлет **Get-AzRmStorageShare** получает или отображает общие файлы хранилища.</span><span class="sxs-lookup"><span data-stu-id="0d575-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="0d575-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d575-112">EXAMPLES</span></span>

### <span data-ttu-id="0d575-113">Пример 1: получение общего файлового хранилища с именем учетной записи хранения и именем общего доступа</span><span class="sxs-lookup"><span data-stu-id="0d575-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="0d575-114">Эта команда возвращает общую файловую систему хранилища с именем учетной записи хранения и именем общего доступа.</span><span class="sxs-lookup"><span data-stu-id="0d575-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="0d575-115">Пример 2: список всех общих файловых ресурсов хранилища для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="0d575-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="0d575-116">Эта команда перечисляет все общие файлы хранилища для учетной записи хранения с именем учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0d575-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="0d575-117">Пример 3: получение контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="0d575-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="0d575-118">Эта команда получает контейнер BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="0d575-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="0d575-119">Пример 4: получение общего файла хранилища с использованием общего доступа в байтах</span><span class="sxs-lookup"><span data-stu-id="0d575-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="0d575-120">Эта команда возвращает общую файловую систему хранения с именем учетной записи хранения и именем общего доступа, а также включает использование общего доступа в байтах.</span><span class="sxs-lookup"><span data-stu-id="0d575-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="0d575-121">Пример 5: список всех общих файловых ресурсов хранилища для учетной записи хранения, включая удаленные общие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="0d575-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="0d575-122">Эта команда выводит список всех общих папок хранилища: удаленные общие ресурсы учетной записи хранения с именем учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0d575-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="0d575-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d575-123">PARAMETERS</span></span>

### <span data-ttu-id="0d575-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d575-124">-DefaultProfile</span></span>
<span data-ttu-id="0d575-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d575-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d575-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="0d575-126">-GetShareUsage</span></span>
<span data-ttu-id="0d575-127">Укажите этот параметр, чтобы получить использование общего доступа в байтах.</span><span class="sxs-lookup"><span data-stu-id="0d575-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameSingle, AccountObjectSingle, ShareResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d575-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="0d575-128">-IncludeDeleted</span></span>
<span data-ttu-id="0d575-129">Включать удаленные общие ресурсы, по умолчанию общие ресурсы не включаются в список "Удаленные".</span><span class="sxs-lookup"><span data-stu-id="0d575-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d575-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d575-130">-Name</span></span>
<span data-ttu-id="0d575-131">Имя общего доступа</span><span class="sxs-lookup"><span data-stu-id="0d575-131">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, ShareResourceId
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountObjectSingle
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d575-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d575-132">-ResourceGroupName</span></span>
<span data-ttu-id="0d575-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d575-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d575-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d575-134">-ResourceId</span></span>
<span data-ttu-id="0d575-135">Введите идентификатор ресурса для общего доступа к файлу.</span><span class="sxs-lookup"><span data-stu-id="0d575-135">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d575-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0d575-136">-StorageAccount</span></span>
<span data-ttu-id="0d575-137">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="0d575-137">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectSingle, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d575-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0d575-138">-StorageAccountName</span></span>
<span data-ttu-id="0d575-139">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0d575-139">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d575-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d575-140">CommonParameters</span></span>
<span data-ttu-id="0d575-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d575-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d575-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d575-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d575-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d575-143">INPUTS</span></span>

### <span data-ttu-id="0d575-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0d575-144">System.String</span></span>

### <span data-ttu-id="0d575-145">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0d575-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="0d575-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d575-146">OUTPUTS</span></span>

### <span data-ttu-id="0d575-147">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="0d575-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="0d575-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d575-148">NOTES</span></span>

## <span data-ttu-id="0d575-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d575-149">RELATED LINKS</span></span>
