---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b1e06a31cfbe16cb04a7158cd62858683db6e131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561276"
---
# <span data-ttu-id="28173-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28173-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="28173-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28173-102">SYNOPSIS</span></span>
<span data-ttu-id="28173-103">Удаляет политику сохраненного доступа из таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="28173-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28173-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28173-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28173-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28173-105">DESCRIPTION</span></span>
<span data-ttu-id="28173-106">Командлет **Remove-AzureStorageTableStoredAccessPolicy** удаляет политику сохраненного доступа из таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="28173-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="28173-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28173-107">EXAMPLES</span></span>

### <span data-ttu-id="28173-108">Пример 1: Удаление политики сохраненных прав доступа из таблицы хранилища</span><span class="sxs-lookup"><span data-stu-id="28173-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="28173-109">Эта команда удаляет политику с именем Policy05 из таблицы хранения с именем MyTable.</span><span class="sxs-lookup"><span data-stu-id="28173-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="28173-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28173-110">PARAMETERS</span></span>

### <span data-ttu-id="28173-111">-Context</span><span class="sxs-lookup"><span data-stu-id="28173-111">-Context</span></span>
<span data-ttu-id="28173-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="28173-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="28173-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="28173-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28173-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28173-114">-DefaultProfile</span></span>
<span data-ttu-id="28173-115">связь с Azure.</span><span class="sxs-lookup"><span data-stu-id="28173-115">communication with Azure.</span></span>

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

### <span data-ttu-id="28173-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28173-116">-PassThru</span></span>
<span data-ttu-id="28173-117">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="28173-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="28173-118">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="28173-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="28173-119">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="28173-119">-Policy</span></span>
<span data-ttu-id="28173-120">Указывает имя политики хранения, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="28173-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28173-121">-Таблица</span><span class="sxs-lookup"><span data-stu-id="28173-121">-Table</span></span>
<span data-ttu-id="28173-122">Указывает имя таблицы Azure.</span><span class="sxs-lookup"><span data-stu-id="28173-122">Specifies the Azure table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28173-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28173-123">-Confirm</span></span>
<span data-ttu-id="28173-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="28173-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28173-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28173-125">-WhatIf</span></span>
<span data-ttu-id="28173-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="28173-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28173-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="28173-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28173-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28173-128">CommonParameters</span></span>
<span data-ttu-id="28173-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28173-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28173-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28173-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28173-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28173-131">INPUTS</span></span>

### <span data-ttu-id="28173-132">System. String</span><span class="sxs-lookup"><span data-stu-id="28173-132">System.String</span></span>

### <span data-ttu-id="28173-133">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="28173-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="28173-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28173-134">OUTPUTS</span></span>

### <span data-ttu-id="28173-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28173-135">System.Boolean</span></span>

## <span data-ttu-id="28173-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="28173-136">NOTES</span></span>

## <span data-ttu-id="28173-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28173-137">RELATED LINKS</span></span>

[<span data-ttu-id="28173-138">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28173-138">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="28173-139">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="28173-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="28173-140">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28173-140">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="28173-141">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28173-141">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
