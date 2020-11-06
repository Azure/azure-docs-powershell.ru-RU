---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8c22b3eb95ab940670043f9ae467663c951027d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556224"
---
# <span data-ttu-id="b3138-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3138-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="b3138-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3138-102">SYNOPSIS</span></span>
<span data-ttu-id="b3138-103">Возвращает политику и политики для сохраненной или политики доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b3138-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b3138-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3138-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3138-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3138-105">DESCRIPTION</span></span>
<span data-ttu-id="b3138-106">Командлет **Get-AzureStorageTableStoredAccessPolicy** включает в себя политику и политики для таблицы хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="b3138-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b3138-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3138-107">EXAMPLES</span></span>

### <span data-ttu-id="b3138-108">Пример 1: получение политики доступа на хранение в таблице хранилища</span><span class="sxs-lookup"><span data-stu-id="b3138-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="b3138-109">Эта команда получает политику доступа с именем Policy50 в таблице хранения данных с именем Table02.</span><span class="sxs-lookup"><span data-stu-id="b3138-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="b3138-110">Пример 2: получение всех сохраненных политик доступа в таблице хранилища</span><span class="sxs-lookup"><span data-stu-id="b3138-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="b3138-111">Эта команда получает все политики доступа в таблице с именем Table02.</span><span class="sxs-lookup"><span data-stu-id="b3138-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="b3138-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3138-112">PARAMETERS</span></span>

### <span data-ttu-id="b3138-113">-Context</span><span class="sxs-lookup"><span data-stu-id="b3138-113">-Context</span></span>
<span data-ttu-id="b3138-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b3138-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b3138-115">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b3138-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b3138-116">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="b3138-116">-Policy</span></span>
<span data-ttu-id="b3138-117">Указывает политику сохраненного доступа, которая включает разрешения для маркера данной подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="b3138-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3138-118">-Таблица</span><span class="sxs-lookup"><span data-stu-id="b3138-118">-Table</span></span>
<span data-ttu-id="b3138-119">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b3138-119">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="b3138-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3138-120">CommonParameters</span></span>
<span data-ttu-id="b3138-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3138-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3138-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3138-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3138-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3138-123">INPUTS</span></span>

## <span data-ttu-id="b3138-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3138-124">OUTPUTS</span></span>

## <span data-ttu-id="b3138-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3138-125">NOTES</span></span>

## <span data-ttu-id="b3138-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3138-126">RELATED LINKS</span></span>

[<span data-ttu-id="b3138-127">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3138-127">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b3138-128">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3138-128">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b3138-129">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3138-129">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b3138-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b3138-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


