---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54b28caaf39bd3d4750e341da4f4564d60b59138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555255"
---
# <span data-ttu-id="8254e-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8254e-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="8254e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8254e-102">SYNOPSIS</span></span>
<span data-ttu-id="8254e-103">Создание политики сохранения для доступа к таблице хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8254e-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="8254e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8254e-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="8254e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8254e-105">DESCRIPTION</span></span>
<span data-ttu-id="8254e-106">Командлет **New-AzureStorageTableStoredAccessPolicy** создает политику сохраненного доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8254e-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="8254e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8254e-107">EXAMPLES</span></span>

### <span data-ttu-id="8254e-108">Пример 1: Создание политики сохраненных прав доступа в таблице</span><span class="sxs-lookup"><span data-stu-id="8254e-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="8254e-109">Эта команда создает политику доступа с именем Policy02 в таблице хранения с именем MyTable.</span><span class="sxs-lookup"><span data-stu-id="8254e-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="8254e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8254e-110">PARAMETERS</span></span>

### <span data-ttu-id="8254e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8254e-111">-Context</span></span>
<span data-ttu-id="8254e-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8254e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8254e-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="8254e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8254e-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8254e-114">-ExpiryTime</span></span>
<span data-ttu-id="8254e-115">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="8254e-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="8254e-116">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="8254e-116">-Permission</span></span>
<span data-ttu-id="8254e-117">Задает уровень общего доступа к этой таблице хранилища.</span><span class="sxs-lookup"><span data-stu-id="8254e-117">Specifies the level of public access to this storage table.</span></span>

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

### <span data-ttu-id="8254e-118">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="8254e-118">-Policy</span></span>
<span data-ttu-id="8254e-119">Указывает политику сохраненного доступа, которая включает разрешения для маркера данной подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="8254e-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="8254e-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8254e-120">-StartTime</span></span>
<span data-ttu-id="8254e-121">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="8254e-121">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="8254e-122">-Таблица</span><span class="sxs-lookup"><span data-stu-id="8254e-122">-Table</span></span>
<span data-ttu-id="8254e-123">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8254e-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="8254e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8254e-124">CommonParameters</span></span>
<span data-ttu-id="8254e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8254e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8254e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8254e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8254e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8254e-127">INPUTS</span></span>

## <span data-ttu-id="8254e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8254e-128">OUTPUTS</span></span>

## <span data-ttu-id="8254e-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="8254e-129">NOTES</span></span>

## <span data-ttu-id="8254e-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8254e-130">RELATED LINKS</span></span>

[<span data-ttu-id="8254e-131">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8254e-131">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="8254e-132">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8254e-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8254e-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8254e-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="8254e-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8254e-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


