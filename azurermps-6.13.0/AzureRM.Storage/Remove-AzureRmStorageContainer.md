---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
ms.openlocfilehash: 089451a0a0aae399a18296fbf4982724b35d432e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734587"
---
# <span data-ttu-id="9e615-101">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9e615-101">Remove-AzureRmStorageContainer</span></span>

## <span data-ttu-id="9e615-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e615-102">SYNOPSIS</span></span>
<span data-ttu-id="9e615-103">Удаляет контейнер BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="9e615-103">Removes a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e615-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e615-104">SYNTAX</span></span>

### <span data-ttu-id="9e615-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e615-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e615-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9e615-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e615-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="9e615-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e615-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e615-108">DESCRIPTION</span></span>
<span data-ttu-id="9e615-109">Командлет **Remove-AzureRmStorageContainer** удаляет контейнер BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="9e615-109">The **Remove-AzureRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="9e615-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e615-110">EXAMPLES</span></span>

### <span data-ttu-id="9e615-111">Пример 1: удаление контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="9e615-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="9e615-112">Эта команда удаляет контейнер BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="9e615-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="9e615-113">Пример 2: удаление контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="9e615-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="9e615-114">Эта команда удаляет контейнер BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="9e615-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="9e615-115">Пример 3. Удаление всех контейнеров BLOB-объектов хранилища в учетной записи хранения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="9e615-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainer -Force
```

<span data-ttu-id="9e615-116">Эта команда удаляет все контейнеры больших двоичных объектов хранилища в учетной записи хранения с конвейером.</span><span class="sxs-lookup"><span data-stu-id="9e615-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="9e615-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e615-117">PARAMETERS</span></span>

### <span data-ttu-id="9e615-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e615-118">-DefaultProfile</span></span>
<span data-ttu-id="9e615-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e615-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e615-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9e615-120">-Force</span></span>
<span data-ttu-id="9e615-121">Принудительное удаление контейнера и всего содержимого</span><span class="sxs-lookup"><span data-stu-id="9e615-121">Force to remove the container and all content in it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e615-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e615-122">-InputObject</span></span>
<span data-ttu-id="9e615-123">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="9e615-123">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e615-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e615-124">-Name</span></span>
<span data-ttu-id="9e615-125">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="9e615-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e615-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e615-126">-PassThru</span></span>
<span data-ttu-id="9e615-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="9e615-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e615-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e615-128">-ResourceGroupName</span></span>
<span data-ttu-id="9e615-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e615-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e615-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9e615-130">-StorageAccount</span></span>
<span data-ttu-id="9e615-131">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9e615-131">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e615-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9e615-132">-StorageAccountName</span></span>
<span data-ttu-id="9e615-133">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9e615-133">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e615-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e615-134">-Confirm</span></span>
<span data-ttu-id="9e615-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e615-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e615-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e615-136">-WhatIf</span></span>
<span data-ttu-id="9e615-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e615-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e615-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e615-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e615-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e615-139">CommonParameters</span></span>
<span data-ttu-id="9e615-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e615-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e615-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e615-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e615-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e615-142">INPUTS</span></span>

### <span data-ttu-id="9e615-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9e615-143">System.String</span></span>

## <span data-ttu-id="9e615-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e615-144">OUTPUTS</span></span>

### <span data-ttu-id="9e615-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="9e615-145">System.Object</span></span>

## <span data-ttu-id="9e615-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e615-146">NOTES</span></span>

## <span data-ttu-id="9e615-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e615-147">RELATED LINKS</span></span>
