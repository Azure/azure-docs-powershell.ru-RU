---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 5a2890f052e57c37ca86197b2fd3841ba3b5c388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567852"
---
# <span data-ttu-id="04dc2-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04dc2-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="04dc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="04dc2-103">Создание политики сохранения для доступа к таблице хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="04dc2-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04dc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04dc2-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04dc2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04dc2-105">DESCRIPTION</span></span>
<span data-ttu-id="04dc2-106">Командлет **New-AzureStorageTableStoredAccessPolicy** создает политику сохраненного доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="04dc2-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="04dc2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04dc2-107">EXAMPLES</span></span>

### <span data-ttu-id="04dc2-108">Пример 1: Создание политики сохраненных прав доступа в таблице</span><span class="sxs-lookup"><span data-stu-id="04dc2-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="04dc2-109">Эта команда создает политику доступа с именем Policy02 в таблице хранения с именем MyTable.</span><span class="sxs-lookup"><span data-stu-id="04dc2-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="04dc2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04dc2-110">PARAMETERS</span></span>

### <span data-ttu-id="04dc2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="04dc2-111">-Context</span></span>
<span data-ttu-id="04dc2-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="04dc2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="04dc2-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="04dc2-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="04dc2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04dc2-114">-DefaultProfile</span></span>
<span data-ttu-id="04dc2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04dc2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04dc2-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="04dc2-116">-ExpiryTime</span></span>
<span data-ttu-id="04dc2-117">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="04dc2-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="04dc2-118">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="04dc2-118">-Permission</span></span>
<span data-ttu-id="04dc2-119">Определяет разрешения в политике сохранения доступа для доступа к таблице хранения.</span><span class="sxs-lookup"><span data-stu-id="04dc2-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="04dc2-120">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="04dc2-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="04dc2-121">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="04dc2-121">-Policy</span></span>
<span data-ttu-id="04dc2-122">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="04dc2-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="04dc2-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="04dc2-123">-StartTime</span></span>
<span data-ttu-id="04dc2-124">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="04dc2-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="04dc2-125">-Таблица</span><span class="sxs-lookup"><span data-stu-id="04dc2-125">-Table</span></span>
<span data-ttu-id="04dc2-126">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="04dc2-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="04dc2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04dc2-127">CommonParameters</span></span>
<span data-ttu-id="04dc2-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04dc2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04dc2-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04dc2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04dc2-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04dc2-130">INPUTS</span></span>

### <span data-ttu-id="04dc2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="04dc2-131">System.String</span></span>

### <span data-ttu-id="04dc2-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="04dc2-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="04dc2-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04dc2-133">OUTPUTS</span></span>

### <span data-ttu-id="04dc2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="04dc2-134">System.String</span></span>

## <span data-ttu-id="04dc2-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="04dc2-135">NOTES</span></span>

## <span data-ttu-id="04dc2-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04dc2-136">RELATED LINKS</span></span>

[<span data-ttu-id="04dc2-137">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04dc2-137">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="04dc2-138">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="04dc2-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="04dc2-139">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04dc2-139">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="04dc2-140">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04dc2-140">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


