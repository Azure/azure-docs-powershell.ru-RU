---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: bff7a79513cc8eb0047860f9edd00c6c37c5f1b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224852"
---
# <span data-ttu-id="6c307-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6c307-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="6c307-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c307-102">SYNOPSIS</span></span>
<span data-ttu-id="6c307-103">Удаляет папку с файлами хранилища.</span><span class="sxs-lookup"><span data-stu-id="6c307-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="6c307-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6c307-104">SYNTAX</span></span>

### <span data-ttu-id="6c307-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c307-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c307-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6c307-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c307-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="6c307-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c307-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="6c307-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c307-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c307-109">DESCRIPTION</span></span>
<span data-ttu-id="6c307-110">Из-за этого удаляется папка хранилища, задав для нее функцию **New-AzRmStorageShare.**</span><span class="sxs-lookup"><span data-stu-id="6c307-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="6c307-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6c307-111">EXAMPLES</span></span>

### <span data-ttu-id="6c307-112">Пример 1. Удаление файла хранилища с именем учетной записи хранения и именем</span><span class="sxs-lookup"><span data-stu-id="6c307-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="6c307-113">Эта команда удаляет файл хранилища с именем и именем учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6c307-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="6c307-114">Пример 2. Удаление файла хранилища с объектом учетной записи хранения и именем</span><span class="sxs-lookup"><span data-stu-id="6c307-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="6c307-115">Эта команда удаляет папку хранилища с объектом учетной записи хранения и именем.</span><span class="sxs-lookup"><span data-stu-id="6c307-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="6c307-116">Пример 3. Удаление всех файлов хранилища в учетной записи хранения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="6c307-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="6c307-117">Эта команда удаляет все папки хранилища в учетной записи хранения с конвейером.</span><span class="sxs-lookup"><span data-stu-id="6c307-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="6c307-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c307-118">PARAMETERS</span></span>

### <span data-ttu-id="6c307-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c307-119">-DefaultProfile</span></span>
<span data-ttu-id="6c307-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c307-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c307-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6c307-121">-Force</span></span>
<span data-ttu-id="6c307-122">Принудительное удаление "Поделиться" и всего содержимого в нем</span><span class="sxs-lookup"><span data-stu-id="6c307-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="6c307-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c307-123">-InputObject</span></span>
<span data-ttu-id="6c307-124">Объект "Поделиться хранилищем"</span><span class="sxs-lookup"><span data-stu-id="6c307-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c307-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6c307-125">-Name</span></span>
<span data-ttu-id="6c307-126">Имя "Поделиться"</span><span class="sxs-lookup"><span data-stu-id="6c307-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c307-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c307-127">-PassThru</span></span>
<span data-ttu-id="6c307-128">Указывает на то, что этот cmdlet возвращает **boolean,** который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="6c307-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="6c307-129">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6c307-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6c307-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c307-130">-ResourceGroupName</span></span>
<span data-ttu-id="6c307-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c307-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c307-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c307-132">-ResourceId</span></span>
<span data-ttu-id="6c307-133">Ввести ИД ресурса для обмена файлами.</span><span class="sxs-lookup"><span data-stu-id="6c307-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="6c307-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c307-134">-StorageAccount</span></span>
<span data-ttu-id="6c307-135">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="6c307-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c307-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6c307-136">-StorageAccountName</span></span>
<span data-ttu-id="6c307-137">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6c307-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c307-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c307-138">-Confirm</span></span>
<span data-ttu-id="6c307-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6c307-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c307-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c307-140">-WhatIf</span></span>
<span data-ttu-id="6c307-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c307-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c307-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6c307-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c307-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c307-143">CommonParameters</span></span>
<span data-ttu-id="6c307-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c307-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c307-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c307-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c307-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c307-146">INPUTS</span></span>

### <span data-ttu-id="6c307-147">System.String</span><span class="sxs-lookup"><span data-stu-id="6c307-147">System.String</span></span>

### <span data-ttu-id="6c307-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c307-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6c307-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="6c307-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="6c307-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c307-150">OUTPUTS</span></span>

### <span data-ttu-id="6c307-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c307-151">System.Boolean</span></span>

## <span data-ttu-id="6c307-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6c307-152">NOTES</span></span>

## <span data-ttu-id="6c307-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c307-153">RELATED LINKS</span></span>
