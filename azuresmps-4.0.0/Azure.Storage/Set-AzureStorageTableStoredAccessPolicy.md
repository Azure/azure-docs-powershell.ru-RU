---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
ms.openlocfilehash: d517ca49f0be3b6add58d151b3b2f79dad17611c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556352"
---
# <span data-ttu-id="b4807-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b4807-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="b4807-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4807-102">SYNOPSIS</span></span>
<span data-ttu-id="b4807-103">Задает политику сохранения для доступа к таблице хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b4807-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="b4807-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4807-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4807-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4807-105">DESCRIPTION</span></span>
<span data-ttu-id="b4807-106">Командлет **Set-AzureStorageTableStoredAccessPolicy** задает политику сохраненных прав доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b4807-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="b4807-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4807-107">EXAMPLES</span></span>

### <span data-ttu-id="b4807-108">Пример 1: Настройка политики доступа в таблице с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="b4807-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08"
```

<span data-ttu-id="b4807-109">Эта команда задает политику доступа с именем Policy08 для таблицы хранения с именем MyTable.</span><span class="sxs-lookup"><span data-stu-id="b4807-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="b4807-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4807-110">PARAMETERS</span></span>

### <span data-ttu-id="b4807-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b4807-111">-Context</span></span>
<span data-ttu-id="b4807-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b4807-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b4807-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b4807-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4807-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b4807-114">-ExpiryTime</span></span>
<span data-ttu-id="b4807-115">Указывает время истечения срока действия политики для сохраненной доступа.</span><span class="sxs-lookup"><span data-stu-id="b4807-115">Specifies the time at which the stored access policy expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4807-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b4807-116">-NoExpiryTime</span></span>
<span data-ttu-id="b4807-117">Указывает на то, что политика доступа не содержит дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="b4807-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="b4807-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="b4807-118">-NoStartTime</span></span>
<span data-ttu-id="b4807-119">Указывает на то, что для времени начала задано значение $Null.</span><span class="sxs-lookup"><span data-stu-id="b4807-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="b4807-120">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="b4807-120">-Permission</span></span>
<span data-ttu-id="b4807-121">Задает уровень общего доступа к этой таблице хранилища.</span><span class="sxs-lookup"><span data-stu-id="b4807-121">Specifies the level of public access to this storage table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4807-122">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="b4807-122">-Policy</span></span>
<span data-ttu-id="b4807-123">Указывает политику сохраненного доступа, которая включает разрешения для этого маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="b4807-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4807-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b4807-124">-StartTime</span></span>
<span data-ttu-id="b4807-125">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="b4807-125">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4807-126">-Таблица</span><span class="sxs-lookup"><span data-stu-id="b4807-126">-Table</span></span>
<span data-ttu-id="b4807-127">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b4807-127">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4807-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4807-128">-Confirm</span></span>
<span data-ttu-id="b4807-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4807-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4807-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4807-130">-WhatIf</span></span>
<span data-ttu-id="b4807-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4807-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4807-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4807-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4807-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4807-133">CommonParameters</span></span>
<span data-ttu-id="b4807-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4807-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4807-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4807-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4807-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4807-136">INPUTS</span></span>

## <span data-ttu-id="b4807-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4807-137">OUTPUTS</span></span>

## <span data-ttu-id="b4807-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4807-138">NOTES</span></span>

## <span data-ttu-id="b4807-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4807-139">RELATED LINKS</span></span>

[<span data-ttu-id="b4807-140">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b4807-140">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b4807-141">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b4807-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b4807-142">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b4807-142">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b4807-143">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b4807-143">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
