---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: e2e1f8952e0b785c5856585ad3e3371074194afd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728593"
---
# <span data-ttu-id="bb5cb-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bb5cb-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="bb5cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="bb5cb-103">Создание политики сохранения для доступа к таблице хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bb5cb-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="bb5cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb5cb-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb5cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb5cb-105">DESCRIPTION</span></span>
<span data-ttu-id="bb5cb-106">Командлет **New-AzStorageTableStoredAccessPolicy** создает политику сохраненного доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bb5cb-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="bb5cb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb5cb-107">EXAMPLES</span></span>

### <span data-ttu-id="bb5cb-108">Пример 1: Создание политики сохраненных прав доступа в таблице</span><span class="sxs-lookup"><span data-stu-id="bb5cb-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="bb5cb-109">Эта команда создает политику доступа с именем Policy02 в таблице хранения с именем MyTable.</span><span class="sxs-lookup"><span data-stu-id="bb5cb-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="bb5cb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb5cb-110">PARAMETERS</span></span>

### <span data-ttu-id="bb5cb-111">-Context</span><span class="sxs-lookup"><span data-stu-id="bb5cb-111">-Context</span></span>
<span data-ttu-id="bb5cb-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bb5cb-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bb5cb-113">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="bb5cb-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bb5cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb5cb-114">-DefaultProfile</span></span>
<span data-ttu-id="bb5cb-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb5cb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5cb-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="bb5cb-116">-ExpiryTime</span></span>
<span data-ttu-id="bb5cb-117">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="bb5cb-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="bb5cb-118">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="bb5cb-118">-Permission</span></span>
<span data-ttu-id="bb5cb-119">Определяет разрешения в политике сохранения доступа для доступа к таблице хранения.</span><span class="sxs-lookup"><span data-stu-id="bb5cb-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="bb5cb-120">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="bb5cb-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="bb5cb-121">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="bb5cb-121">-Policy</span></span>
<span data-ttu-id="bb5cb-122">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="bb5cb-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="bb5cb-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bb5cb-123">-StartTime</span></span>
<span data-ttu-id="bb5cb-124">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="bb5cb-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="bb5cb-125">-Таблица</span><span class="sxs-lookup"><span data-stu-id="bb5cb-125">-Table</span></span>
<span data-ttu-id="bb5cb-126">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bb5cb-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="bb5cb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb5cb-127">CommonParameters</span></span>
<span data-ttu-id="bb5cb-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb5cb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb5cb-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb5cb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb5cb-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb5cb-130">INPUTS</span></span>

### <span data-ttu-id="bb5cb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bb5cb-131">System.String</span></span>

### <span data-ttu-id="bb5cb-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bb5cb-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bb5cb-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb5cb-133">OUTPUTS</span></span>

### <span data-ttu-id="bb5cb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bb5cb-134">System.String</span></span>

## <span data-ttu-id="bb5cb-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb5cb-135">NOTES</span></span>

## <span data-ttu-id="bb5cb-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb5cb-136">RELATED LINKS</span></span>

[<span data-ttu-id="bb5cb-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bb5cb-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="bb5cb-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="bb5cb-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="bb5cb-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bb5cb-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="bb5cb-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bb5cb-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


