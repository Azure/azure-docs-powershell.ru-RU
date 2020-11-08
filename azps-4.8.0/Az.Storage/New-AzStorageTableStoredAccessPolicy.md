---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 82e5d252e2e8185b98c142b24537c666e5618d7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236544"
---
# <span data-ttu-id="fd2e0-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fd2e0-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="fd2e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd2e0-102">SYNOPSIS</span></span>
<span data-ttu-id="fd2e0-103">Создание политики сохранения для доступа к таблице хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fd2e0-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="fd2e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd2e0-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd2e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd2e0-105">DESCRIPTION</span></span>
<span data-ttu-id="fd2e0-106">Командлет **New-AzStorageTableStoredAccessPolicy** создает политику сохраненного доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fd2e0-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="fd2e0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd2e0-107">EXAMPLES</span></span>

### <span data-ttu-id="fd2e0-108">Пример 1: Создание политики сохраненных прав доступа в таблице</span><span class="sxs-lookup"><span data-stu-id="fd2e0-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="fd2e0-109">Эта команда создает политику доступа с именем Policy02 в таблице хранения с именем MyTable.</span><span class="sxs-lookup"><span data-stu-id="fd2e0-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="fd2e0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd2e0-110">PARAMETERS</span></span>

### <span data-ttu-id="fd2e0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="fd2e0-111">-Context</span></span>
<span data-ttu-id="fd2e0-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fd2e0-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fd2e0-113">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fd2e0-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fd2e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd2e0-114">-DefaultProfile</span></span>
<span data-ttu-id="fd2e0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd2e0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd2e0-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fd2e0-116">-ExpiryTime</span></span>
<span data-ttu-id="fd2e0-117">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="fd2e0-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="fd2e0-118">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="fd2e0-118">-Permission</span></span>
<span data-ttu-id="fd2e0-119">Определяет разрешения в политике сохранения доступа для доступа к таблице хранения.</span><span class="sxs-lookup"><span data-stu-id="fd2e0-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="fd2e0-120">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="fd2e0-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="fd2e0-121">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="fd2e0-121">-Policy</span></span>
<span data-ttu-id="fd2e0-122">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="fd2e0-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="fd2e0-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fd2e0-123">-StartTime</span></span>
<span data-ttu-id="fd2e0-124">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="fd2e0-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="fd2e0-125">-Таблица</span><span class="sxs-lookup"><span data-stu-id="fd2e0-125">-Table</span></span>
<span data-ttu-id="fd2e0-126">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fd2e0-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="fd2e0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd2e0-127">CommonParameters</span></span>
<span data-ttu-id="fd2e0-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd2e0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd2e0-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd2e0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd2e0-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd2e0-130">INPUTS</span></span>

### <span data-ttu-id="fd2e0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fd2e0-131">System.String</span></span>

### <span data-ttu-id="fd2e0-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fd2e0-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fd2e0-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd2e0-133">OUTPUTS</span></span>

### <span data-ttu-id="fd2e0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fd2e0-134">System.String</span></span>

## <span data-ttu-id="fd2e0-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd2e0-135">NOTES</span></span>

## <span data-ttu-id="fd2e0-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd2e0-136">RELATED LINKS</span></span>

[<span data-ttu-id="fd2e0-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fd2e0-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fd2e0-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fd2e0-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="fd2e0-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fd2e0-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fd2e0-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fd2e0-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


