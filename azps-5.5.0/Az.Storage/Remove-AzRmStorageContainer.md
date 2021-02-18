---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 333df1432ed892e75e0b798f1412cb7b0327a334
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224876"
---
# <span data-ttu-id="2783f-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2783f-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="2783f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2783f-102">SYNOPSIS</span></span>
<span data-ttu-id="2783f-103">Удаление контейнера BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="2783f-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="2783f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2783f-104">SYNTAX</span></span>

### <span data-ttu-id="2783f-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2783f-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2783f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2783f-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2783f-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="2783f-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2783f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2783f-108">DESCRIPTION</span></span>
<span data-ttu-id="2783f-109">Для **удаления контейнера BLOB-хранилищ удаляется проектлет Remove-AzRmStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="2783f-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="2783f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2783f-110">EXAMPLES</span></span>

### <span data-ttu-id="2783f-111">Пример 1. Удаление контейнера BLOB-хранилищ с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="2783f-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="2783f-112">Эта команда удаляет контейнер BLOB-хранилищ с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="2783f-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="2783f-113">Пример 2. Удаление контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="2783f-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="2783f-114">Эта команда удаляет контейнер BLOB-объектов хранилища с именем объекта учетной записи хранения и контейнера.</span><span class="sxs-lookup"><span data-stu-id="2783f-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="2783f-115">Пример 3. Удаление всех контейнеров BLOB-проектов хранилища в учетной записи хранения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="2783f-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="2783f-116">Эта команда удаляет все контейнеры BLOB-проектов хранилища в учетной записи хранения с конвейером.</span><span class="sxs-lookup"><span data-stu-id="2783f-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="2783f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2783f-117">PARAMETERS</span></span>

### <span data-ttu-id="2783f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2783f-118">-DefaultProfile</span></span>
<span data-ttu-id="2783f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2783f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2783f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2783f-120">-Force</span></span>
<span data-ttu-id="2783f-121">Принудительное удаление контейнера и всего содержимого в нем</span><span class="sxs-lookup"><span data-stu-id="2783f-121">Force to remove the container and all content in it</span></span>

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

### <span data-ttu-id="2783f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2783f-122">-InputObject</span></span>
<span data-ttu-id="2783f-123">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="2783f-123">Storage container object</span></span>

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

### <span data-ttu-id="2783f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2783f-124">-Name</span></span>
<span data-ttu-id="2783f-125">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="2783f-125">Container Name</span></span>

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

### <span data-ttu-id="2783f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2783f-126">-PassThru</span></span>
<span data-ttu-id="2783f-127">Указывает на то, что этот cmdlet возвращает **boolean,** который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="2783f-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="2783f-128">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2783f-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2783f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2783f-129">-ResourceGroupName</span></span>
<span data-ttu-id="2783f-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2783f-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="2783f-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2783f-131">-StorageAccount</span></span>
<span data-ttu-id="2783f-132">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="2783f-132">Storage account object</span></span>

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

### <span data-ttu-id="2783f-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2783f-133">-StorageAccountName</span></span>
<span data-ttu-id="2783f-134">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2783f-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="2783f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2783f-135">-Confirm</span></span>
<span data-ttu-id="2783f-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2783f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2783f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2783f-137">-WhatIf</span></span>
<span data-ttu-id="2783f-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2783f-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2783f-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2783f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2783f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2783f-140">CommonParameters</span></span>
<span data-ttu-id="2783f-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2783f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2783f-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2783f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2783f-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2783f-143">INPUTS</span></span>

### <span data-ttu-id="2783f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2783f-144">System.String</span></span>

### <span data-ttu-id="2783f-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2783f-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="2783f-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="2783f-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="2783f-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2783f-147">OUTPUTS</span></span>

### <span data-ttu-id="2783f-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2783f-148">System.Boolean</span></span>

## <span data-ttu-id="2783f-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2783f-149">NOTES</span></span>

## <span data-ttu-id="2783f-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2783f-150">RELATED LINKS</span></span>
