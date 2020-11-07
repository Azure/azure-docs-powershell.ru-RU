---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: fe98eee14797ff26c39b003d8ab1c9826c8ec687
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910653"
---
# <span data-ttu-id="4593d-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4593d-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="4593d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4593d-102">SYNOPSIS</span></span>
<span data-ttu-id="4593d-103">Задает политику сохранения для доступа к таблице хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4593d-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="4593d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4593d-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4593d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4593d-105">DESCRIPTION</span></span>
<span data-ttu-id="4593d-106">Командлет **Set-AzStorageTableStoredAccessPolicy** задает политику сохраненных прав доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4593d-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="4593d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4593d-107">EXAMPLES</span></span>

### <span data-ttu-id="4593d-108">Пример 1: Настройка политики доступа в таблице с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="4593d-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="4593d-109">Эта команда задает политику доступа с именем Policy08 для таблицы хранения с именем MyTable.</span><span class="sxs-lookup"><span data-stu-id="4593d-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="4593d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4593d-110">PARAMETERS</span></span>

### <span data-ttu-id="4593d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4593d-111">-Context</span></span>
<span data-ttu-id="4593d-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4593d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4593d-113">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4593d-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4593d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4593d-114">-DefaultProfile</span></span>
<span data-ttu-id="4593d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4593d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4593d-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4593d-116">-ExpiryTime</span></span>
<span data-ttu-id="4593d-117">Указывает время истечения срока действия политики для сохраненной доступа.</span><span class="sxs-lookup"><span data-stu-id="4593d-117">Specifies the time at which the stored access policy expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4593d-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4593d-118">-NoExpiryTime</span></span>
<span data-ttu-id="4593d-119">Указывает на то, что политика доступа не содержит дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="4593d-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="4593d-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="4593d-120">-NoStartTime</span></span>
<span data-ttu-id="4593d-121">Указывает на то, что для времени начала задано значение $Null.</span><span class="sxs-lookup"><span data-stu-id="4593d-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="4593d-122">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="4593d-122">-Permission</span></span>
<span data-ttu-id="4593d-123">Определяет разрешения в политике сохранения доступа для доступа к таблице хранения.</span><span class="sxs-lookup"><span data-stu-id="4593d-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="4593d-124">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="4593d-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4593d-125">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="4593d-125">-Policy</span></span>
<span data-ttu-id="4593d-126">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="4593d-126">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4593d-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4593d-127">-StartTime</span></span>
<span data-ttu-id="4593d-128">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="4593d-128">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4593d-129">-Таблица</span><span class="sxs-lookup"><span data-stu-id="4593d-129">-Table</span></span>
<span data-ttu-id="4593d-130">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4593d-130">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4593d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4593d-131">-Confirm</span></span>
<span data-ttu-id="4593d-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4593d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4593d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4593d-133">-WhatIf</span></span>
<span data-ttu-id="4593d-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4593d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4593d-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4593d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4593d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4593d-136">CommonParameters</span></span>
<span data-ttu-id="4593d-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4593d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4593d-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4593d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4593d-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4593d-139">INPUTS</span></span>

### <span data-ttu-id="4593d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4593d-140">System.String</span></span>

### <span data-ttu-id="4593d-141">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4593d-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4593d-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4593d-142">OUTPUTS</span></span>

### <span data-ttu-id="4593d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4593d-143">System.String</span></span>

## <span data-ttu-id="4593d-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="4593d-144">NOTES</span></span>

## <span data-ttu-id="4593d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4593d-145">RELATED LINKS</span></span>

[<span data-ttu-id="4593d-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4593d-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4593d-147">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4593d-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4593d-148">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4593d-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4593d-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4593d-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
