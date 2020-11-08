---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 333df1432ed892e75e0b798f1412cb7b0327a334
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249335"
---
# <span data-ttu-id="607ea-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="607ea-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="607ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="607ea-102">SYNOPSIS</span></span>
<span data-ttu-id="607ea-103">Удаляет контейнер BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="607ea-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="607ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="607ea-104">SYNTAX</span></span>

### <span data-ttu-id="607ea-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="607ea-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="607ea-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="607ea-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="607ea-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="607ea-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="607ea-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="607ea-108">DESCRIPTION</span></span>
<span data-ttu-id="607ea-109">Командлет **Remove-AzRmStorageContainer** удаляет контейнер BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="607ea-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="607ea-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="607ea-110">EXAMPLES</span></span>

### <span data-ttu-id="607ea-111">Пример 1: удаление контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="607ea-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="607ea-112">Эта команда удаляет контейнер BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="607ea-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="607ea-113">Пример 2: удаление контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="607ea-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="607ea-114">Эта команда удаляет контейнер BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="607ea-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="607ea-115">Пример 3. Удаление всех контейнеров BLOB-объектов хранилища в учетной записи хранения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="607ea-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="607ea-116">Эта команда удаляет все контейнеры больших двоичных объектов хранилища в учетной записи хранения с конвейером.</span><span class="sxs-lookup"><span data-stu-id="607ea-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="607ea-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="607ea-117">PARAMETERS</span></span>

### <span data-ttu-id="607ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="607ea-118">-DefaultProfile</span></span>
<span data-ttu-id="607ea-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="607ea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="607ea-120">-Force</span><span class="sxs-lookup"><span data-stu-id="607ea-120">-Force</span></span>
<span data-ttu-id="607ea-121">Принудительное удаление контейнера и всего содержимого</span><span class="sxs-lookup"><span data-stu-id="607ea-121">Force to remove the container and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607ea-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="607ea-122">-InputObject</span></span>
<span data-ttu-id="607ea-123">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="607ea-123">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="607ea-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="607ea-124">-Name</span></span>
<span data-ttu-id="607ea-125">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="607ea-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="607ea-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="607ea-126">-PassThru</span></span>
<span data-ttu-id="607ea-127">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="607ea-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="607ea-128">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="607ea-128">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607ea-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="607ea-129">-ResourceGroupName</span></span>
<span data-ttu-id="607ea-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="607ea-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="607ea-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="607ea-131">-StorageAccount</span></span>
<span data-ttu-id="607ea-132">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="607ea-132">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="607ea-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="607ea-133">-StorageAccountName</span></span>
<span data-ttu-id="607ea-134">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="607ea-134">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="607ea-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="607ea-135">-Confirm</span></span>
<span data-ttu-id="607ea-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="607ea-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607ea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="607ea-137">-WhatIf</span></span>
<span data-ttu-id="607ea-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="607ea-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="607ea-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="607ea-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607ea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="607ea-140">CommonParameters</span></span>
<span data-ttu-id="607ea-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="607ea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="607ea-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="607ea-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="607ea-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="607ea-143">INPUTS</span></span>

### <span data-ttu-id="607ea-144">System. String</span><span class="sxs-lookup"><span data-stu-id="607ea-144">System.String</span></span>

### <span data-ttu-id="607ea-145">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="607ea-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="607ea-146">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="607ea-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="607ea-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="607ea-147">OUTPUTS</span></span>

### <span data-ttu-id="607ea-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="607ea-148">System.Boolean</span></span>

## <span data-ttu-id="607ea-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="607ea-149">NOTES</span></span>

## <span data-ttu-id="607ea-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="607ea-150">RELATED LINKS</span></span>
