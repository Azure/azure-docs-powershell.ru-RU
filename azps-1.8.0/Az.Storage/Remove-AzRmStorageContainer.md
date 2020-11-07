---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: d7a4563a32da28215dbb9b6dab2b911a500183a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728587"
---
# <span data-ttu-id="8dd69-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8dd69-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="8dd69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dd69-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd69-103">Удаляет контейнер BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8dd69-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="8dd69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dd69-104">SYNTAX</span></span>

### <span data-ttu-id="8dd69-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dd69-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dd69-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8dd69-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dd69-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="8dd69-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dd69-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dd69-108">DESCRIPTION</span></span>
<span data-ttu-id="8dd69-109">Командлет **Remove-AzRmStorageContainer** удаляет контейнер BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8dd69-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="8dd69-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dd69-110">EXAMPLES</span></span>

### <span data-ttu-id="8dd69-111">Пример 1: удаление контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="8dd69-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="8dd69-112">Эта команда удаляет контейнер BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="8dd69-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="8dd69-113">Пример 2: удаление контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="8dd69-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="8dd69-114">Эта команда удаляет контейнер BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="8dd69-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="8dd69-115">Пример 3. Удаление всех контейнеров BLOB-объектов хранилища в учетной записи хранения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="8dd69-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="8dd69-116">Эта команда удаляет все контейнеры больших двоичных объектов хранилища в учетной записи хранения с конвейером.</span><span class="sxs-lookup"><span data-stu-id="8dd69-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="8dd69-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dd69-117">PARAMETERS</span></span>

### <span data-ttu-id="8dd69-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd69-118">-DefaultProfile</span></span>
<span data-ttu-id="8dd69-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd69-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dd69-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8dd69-120">-Force</span></span>
<span data-ttu-id="8dd69-121">Принудительное удаление контейнера и всего содержимого</span><span class="sxs-lookup"><span data-stu-id="8dd69-121">Force to remove the container and all content in it</span></span>

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

### <span data-ttu-id="8dd69-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dd69-122">-InputObject</span></span>
<span data-ttu-id="8dd69-123">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="8dd69-123">Storage container object</span></span>

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

### <span data-ttu-id="8dd69-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8dd69-124">-Name</span></span>
<span data-ttu-id="8dd69-125">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="8dd69-125">Container Name</span></span>

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

### <span data-ttu-id="8dd69-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dd69-126">-PassThru</span></span>
<span data-ttu-id="8dd69-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="8dd69-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8dd69-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd69-128">-ResourceGroupName</span></span>
<span data-ttu-id="8dd69-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8dd69-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="8dd69-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8dd69-130">-StorageAccount</span></span>
<span data-ttu-id="8dd69-131">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8dd69-131">Storage account object</span></span>

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

### <span data-ttu-id="8dd69-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8dd69-132">-StorageAccountName</span></span>
<span data-ttu-id="8dd69-133">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8dd69-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="8dd69-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dd69-134">-Confirm</span></span>
<span data-ttu-id="8dd69-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8dd69-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dd69-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dd69-136">-WhatIf</span></span>
<span data-ttu-id="8dd69-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8dd69-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dd69-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8dd69-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dd69-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd69-139">CommonParameters</span></span>
<span data-ttu-id="8dd69-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dd69-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd69-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dd69-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd69-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dd69-142">INPUTS</span></span>

### <span data-ttu-id="8dd69-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8dd69-143">System.String</span></span>

### <span data-ttu-id="8dd69-144">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8dd69-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8dd69-145">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="8dd69-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="8dd69-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dd69-146">OUTPUTS</span></span>

### <span data-ttu-id="8dd69-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8dd69-147">System.Boolean</span></span>

## <span data-ttu-id="8dd69-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dd69-148">NOTES</span></span>

## <span data-ttu-id="8dd69-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dd69-149">RELATED LINKS</span></span>
