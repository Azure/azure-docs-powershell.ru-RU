---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 90edd254eb77b03f4f4d26761020d71025960426
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325096"
---
# <span data-ttu-id="cfa49-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cfa49-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="cfa49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfa49-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa49-103">Возвращает или перечисляет папки с файлами хранилища.</span><span class="sxs-lookup"><span data-stu-id="cfa49-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="cfa49-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cfa49-104">SYNTAX</span></span>

### <span data-ttu-id="cfa49-105">AccountNameSingle (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cfa49-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfa49-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="cfa49-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfa49-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="cfa49-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfa49-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cfa49-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfa49-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="cfa49-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfa49-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfa49-110">DESCRIPTION</span></span>
<span data-ttu-id="cfa49-111">Для **получения или перечисления** файлового списка можно получить или перечислить все папки, хранимые в хранилище.</span><span class="sxs-lookup"><span data-stu-id="cfa49-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="cfa49-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cfa49-112">EXAMPLES</span></span>

### <span data-ttu-id="cfa49-113">Пример 1. Получить файл хранилища с именем учетной записи хранения и именем</span><span class="sxs-lookup"><span data-stu-id="cfa49-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="cfa49-114">Эта команда получает папку хранилища с именем учетной записи хранения и именем в совместном хранении.</span><span class="sxs-lookup"><span data-stu-id="cfa49-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="cfa49-115">Пример 2. Список всех файлов хранилища в папках учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="cfa49-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="cfa49-116">В этой команде перечислены все папки хранилища учетной записи хранения с именем учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cfa49-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="cfa49-117">Пример 3. Получите контейнер BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="cfa49-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="cfa49-118">Эта команда получает контейнер BLOB-объектов хранилища с именем объекта учетной записи хранения и контейнера.</span><span class="sxs-lookup"><span data-stu-id="cfa49-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="cfa49-119">Пример 4. Получить файл хранилища с использованием в этих папках</span><span class="sxs-lookup"><span data-stu-id="cfa49-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="cfa49-120">Эта команда получает файл хранилища с именем учетной записи хранения и именем, а также включает использование папки в bytes.</span><span class="sxs-lookup"><span data-stu-id="cfa49-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="cfa49-121">Пример 5. Список всех файлов хранилища в учетной записи хранения, включая удаленные папки</span><span class="sxs-lookup"><span data-stu-id="cfa49-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="cfa49-122">Эта команда содержит список всех файлов хранилища, включая удаленные папки учетной записи хранения с именем учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cfa49-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="cfa49-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfa49-123">PARAMETERS</span></span>

### <span data-ttu-id="cfa49-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa49-124">-DefaultProfile</span></span>
<span data-ttu-id="cfa49-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa49-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfa49-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="cfa49-126">-GetShareUsage</span></span>
<span data-ttu-id="cfa49-127">Укажите этот параметр, чтобы получить параметр "Поделиться использованием в bytes".</span><span class="sxs-lookup"><span data-stu-id="cfa49-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

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

### <span data-ttu-id="cfa49-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="cfa49-128">-IncludeDeleted</span></span>
<span data-ttu-id="cfa49-129">Включайте удаленные акции, по умолчанию они не включают удаленные акции</span><span class="sxs-lookup"><span data-stu-id="cfa49-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

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

### <span data-ttu-id="cfa49-130">-Name</span><span class="sxs-lookup"><span data-stu-id="cfa49-130">-Name</span></span>
<span data-ttu-id="cfa49-131">Имя "Поделиться"</span><span class="sxs-lookup"><span data-stu-id="cfa49-131">Share Name</span></span>

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

### <span data-ttu-id="cfa49-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfa49-132">-ResourceGroupName</span></span>
<span data-ttu-id="cfa49-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cfa49-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="cfa49-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfa49-134">-ResourceId</span></span>
<span data-ttu-id="cfa49-135">Ввести ИД ресурса для обмена файлами.</span><span class="sxs-lookup"><span data-stu-id="cfa49-135">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="cfa49-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa49-136">-StorageAccount</span></span>
<span data-ttu-id="cfa49-137">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="cfa49-137">Storage account object</span></span>

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

### <span data-ttu-id="cfa49-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cfa49-138">-StorageAccountName</span></span>
<span data-ttu-id="cfa49-139">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cfa49-139">Storage Account Name.</span></span>

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

### <span data-ttu-id="cfa49-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa49-140">CommonParameters</span></span>
<span data-ttu-id="cfa49-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfa49-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa49-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfa49-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa49-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cfa49-143">INPUTS</span></span>

### <span data-ttu-id="cfa49-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cfa49-144">System.String</span></span>

### <span data-ttu-id="cfa49-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa49-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="cfa49-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cfa49-146">OUTPUTS</span></span>

### <span data-ttu-id="cfa49-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="cfa49-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="cfa49-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cfa49-148">NOTES</span></span>

## <span data-ttu-id="cfa49-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfa49-149">RELATED LINKS</span></span>
