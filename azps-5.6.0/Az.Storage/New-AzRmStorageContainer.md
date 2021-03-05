---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: c85b482ff077263d20ae770e6ec6d91b497153e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994759"
---
# <span data-ttu-id="196ad-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="196ad-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="196ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="196ad-102">SYNOPSIS</span></span>
<span data-ttu-id="196ad-103">Создание контейнера BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="196ad-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="196ad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="196ad-104">SYNTAX</span></span>

### <span data-ttu-id="196ad-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="196ad-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="196ad-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="196ad-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="196ad-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="196ad-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="196ad-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="196ad-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="196ad-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="196ad-109">DESCRIPTION</span></span>
<span data-ttu-id="196ad-110">Для создания контейнера BLOB-lob-хранилища создается проектлет **New-AzRmStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="196ad-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="196ad-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="196ad-111">EXAMPLES</span></span>

### <span data-ttu-id="196ad-112">Пример 1. Создание контейнера BLOB-хранилищ с именем учетной записи хранения и именем контейнера с метаданными</span><span class="sxs-lookup"><span data-stu-id="196ad-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="196ad-113">Эта команда создает контейнер BLOB-хранилищ с именем учетной записи хранения и именем контейнера с метаданными.</span><span class="sxs-lookup"><span data-stu-id="196ad-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="196ad-114">Пример 2. Создание контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера с общедоступным доступом в качестве BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="196ad-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="196ad-115">Эта команда создает контейнер BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера с общедоступным доступом в качестве BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="196ad-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="196ad-116">Пример 3. Создание контейнера хранилища с параметром EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="196ad-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
```
PS C:\> $c = New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name testcontainer -DefaultEncryptionScope "testscope" -PreventEncryptionScopeOverride $true

PS C:\> $c

   ResourceGroupName: myResourceGroup, StorageAccountName: myStorageAccount

Name          PublicAccess LastModified HasLegalHold HasImmutabilityPolicy
----          ------------ ------------ ------------ ---------------------
testcontainer                           False        False                

PS C:\> $c.DefaultEncryptionScope
testscope

PS C:\> $c.DenyEncryptionScopeOverride
True
```

<span data-ttu-id="196ad-117">Эта команда создает контейнер хранилища с де defalt encryptionScope и блокирует переопределения области шифрования, заданной по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="196ad-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="196ad-118">Затем откажите свойства связанного контейнера.</span><span class="sxs-lookup"><span data-stu-id="196ad-118">Then show the related container properties.</span></span>

## <span data-ttu-id="196ad-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="196ad-119">PARAMETERS</span></span>

### <span data-ttu-id="196ad-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="196ad-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="196ad-121">Используется по умолчанию для всех записей с заданной областью шифрования.</span><span class="sxs-lookup"><span data-stu-id="196ad-121">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196ad-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196ad-122">-DefaultProfile</span></span>
<span data-ttu-id="196ad-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="196ad-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="196ad-124">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="196ad-124">-Metadata</span></span>
<span data-ttu-id="196ad-125">Метаданные контейнера</span><span class="sxs-lookup"><span data-stu-id="196ad-125">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196ad-126">-Name</span><span class="sxs-lookup"><span data-stu-id="196ad-126">-Name</span></span>
<span data-ttu-id="196ad-127">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="196ad-127">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="196ad-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="196ad-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="196ad-129">Заблокировать переопределения области шифрования, заданную по умолчанию для контейнера.</span><span class="sxs-lookup"><span data-stu-id="196ad-129">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196ad-130">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="196ad-130">-PublicAccess</span></span>
<span data-ttu-id="196ad-131">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="196ad-131">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="196ad-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="196ad-132">-ResourceGroupName</span></span>
<span data-ttu-id="196ad-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="196ad-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="196ad-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="196ad-134">-StorageAccount</span></span>
<span data-ttu-id="196ad-135">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="196ad-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="196ad-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="196ad-136">-StorageAccountName</span></span>
<span data-ttu-id="196ad-137">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="196ad-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="196ad-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="196ad-138">-Confirm</span></span>
<span data-ttu-id="196ad-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="196ad-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="196ad-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="196ad-140">-WhatIf</span></span>
<span data-ttu-id="196ad-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="196ad-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="196ad-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="196ad-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="196ad-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196ad-143">CommonParameters</span></span>
<span data-ttu-id="196ad-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="196ad-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196ad-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="196ad-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196ad-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="196ad-146">INPUTS</span></span>

### <span data-ttu-id="196ad-147">System.String</span><span class="sxs-lookup"><span data-stu-id="196ad-147">System.String</span></span>

### <span data-ttu-id="196ad-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="196ad-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="196ad-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="196ad-149">OUTPUTS</span></span>

### <span data-ttu-id="196ad-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="196ad-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="196ad-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="196ad-151">NOTES</span></span>

## <span data-ttu-id="196ad-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="196ad-152">RELATED LINKS</span></span>
