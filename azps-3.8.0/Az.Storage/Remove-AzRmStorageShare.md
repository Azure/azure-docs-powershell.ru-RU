---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: bff7a79513cc8eb0047860f9edd00c6c37c5f1b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066931"
---
# <span data-ttu-id="508aa-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="508aa-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="508aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="508aa-102">SYNOPSIS</span></span>
<span data-ttu-id="508aa-103">Удаляет файловый общий доступ к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="508aa-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="508aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="508aa-104">SYNTAX</span></span>

### <span data-ttu-id="508aa-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="508aa-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="508aa-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="508aa-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="508aa-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="508aa-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="508aa-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="508aa-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="508aa-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="508aa-109">DESCRIPTION</span></span>
<span data-ttu-id="508aa-110">Командлет **New-AzRmStorageShare** удаляет файловый общий доступ к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="508aa-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="508aa-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="508aa-111">EXAMPLES</span></span>

### <span data-ttu-id="508aa-112">Пример 1: Удаление общей файловой системы хранения с именем учетной записи хранения и именем общего доступа</span><span class="sxs-lookup"><span data-stu-id="508aa-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="508aa-113">Эта команда удаляет общую файловую систему хранилища с именем учетной записи хранения и именем общего доступа.</span><span class="sxs-lookup"><span data-stu-id="508aa-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="508aa-114">Пример 2: Удаление общей файловой системы хранения с объектом учетной записи хранения и именем общего доступа</span><span class="sxs-lookup"><span data-stu-id="508aa-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="508aa-115">Эта команда удаляет общую файловую систему хранилища с объектом учетной записи хранения и именем общего доступа.</span><span class="sxs-lookup"><span data-stu-id="508aa-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="508aa-116">Пример 3. Удаление всех общих файлов хранилища в учетной записи хранения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="508aa-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="508aa-117">Эта команда удаляет все общие файлы хранилища в учетной записи хранения с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="508aa-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="508aa-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="508aa-118">PARAMETERS</span></span>

### <span data-ttu-id="508aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="508aa-119">-DefaultProfile</span></span>
<span data-ttu-id="508aa-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="508aa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="508aa-121">-Force</span><span class="sxs-lookup"><span data-stu-id="508aa-121">-Force</span></span>
<span data-ttu-id="508aa-122">Принудительное удаление общего доступа и всего содержимого</span><span class="sxs-lookup"><span data-stu-id="508aa-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="508aa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="508aa-123">-InputObject</span></span>
<span data-ttu-id="508aa-124">Объект общего доступа к хранилищу</span><span class="sxs-lookup"><span data-stu-id="508aa-124">Storage Share object</span></span>

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

### <span data-ttu-id="508aa-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="508aa-125">-Name</span></span>
<span data-ttu-id="508aa-126">Имя общего доступа</span><span class="sxs-lookup"><span data-stu-id="508aa-126">Share Name</span></span>

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

### <span data-ttu-id="508aa-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="508aa-127">-PassThru</span></span>
<span data-ttu-id="508aa-128">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="508aa-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="508aa-129">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="508aa-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="508aa-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="508aa-130">-ResourceGroupName</span></span>
<span data-ttu-id="508aa-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="508aa-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="508aa-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="508aa-132">-ResourceId</span></span>
<span data-ttu-id="508aa-133">Введите идентификатор ресурса для общего доступа к файлу.</span><span class="sxs-lookup"><span data-stu-id="508aa-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="508aa-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="508aa-134">-StorageAccount</span></span>
<span data-ttu-id="508aa-135">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="508aa-135">Storage account object</span></span>

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

### <span data-ttu-id="508aa-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="508aa-136">-StorageAccountName</span></span>
<span data-ttu-id="508aa-137">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="508aa-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="508aa-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="508aa-138">-Confirm</span></span>
<span data-ttu-id="508aa-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="508aa-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="508aa-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="508aa-140">-WhatIf</span></span>
<span data-ttu-id="508aa-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="508aa-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="508aa-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="508aa-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="508aa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="508aa-143">CommonParameters</span></span>
<span data-ttu-id="508aa-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="508aa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="508aa-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="508aa-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="508aa-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="508aa-146">INPUTS</span></span>

### <span data-ttu-id="508aa-147">System. String</span><span class="sxs-lookup"><span data-stu-id="508aa-147">System.String</span></span>

### <span data-ttu-id="508aa-148">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="508aa-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="508aa-149">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="508aa-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="508aa-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="508aa-150">OUTPUTS</span></span>

### <span data-ttu-id="508aa-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="508aa-151">System.Boolean</span></span>

## <span data-ttu-id="508aa-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="508aa-152">NOTES</span></span>

## <span data-ttu-id="508aa-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="508aa-153">RELATED LINKS</span></span>
