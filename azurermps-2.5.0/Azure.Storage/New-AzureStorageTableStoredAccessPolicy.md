---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 21e289ce0a8e7ca2d430d64ab9cc75bfd0c1a3ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914966"
---
# <span data-ttu-id="67ace-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="67ace-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="67ace-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67ace-102">SYNOPSIS</span></span>
<span data-ttu-id="67ace-103">Создание политики сохранения для доступа к таблице хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="67ace-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67ace-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67ace-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67ace-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67ace-105">DESCRIPTION</span></span>
<span data-ttu-id="67ace-106">Командлет **New-AzureStorageTableStoredAccessPolicy** создает политику сохраненного доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="67ace-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="67ace-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67ace-107">EXAMPLES</span></span>

### <span data-ttu-id="67ace-108">Пример 1: Создание политики сохраненных прав доступа в таблице</span><span class="sxs-lookup"><span data-stu-id="67ace-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="67ace-109">Эта команда создает политику доступа с именем Policy02 в таблице хранения с именем MyTable.</span><span class="sxs-lookup"><span data-stu-id="67ace-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="67ace-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67ace-110">PARAMETERS</span></span>

### <span data-ttu-id="67ace-111">-Context</span><span class="sxs-lookup"><span data-stu-id="67ace-111">-Context</span></span>
<span data-ttu-id="67ace-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="67ace-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="67ace-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="67ace-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="67ace-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ace-114">-DefaultProfile</span></span>
<span data-ttu-id="67ace-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67ace-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ace-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="67ace-116">-ExpiryTime</span></span>
<span data-ttu-id="67ace-117">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="67ace-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="67ace-118">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="67ace-118">-Permission</span></span>
<span data-ttu-id="67ace-119">Определяет разрешения в политике сохранения доступа для доступа к таблице хранения.</span><span class="sxs-lookup"><span data-stu-id="67ace-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="67ace-120">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="67ace-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="67ace-121">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="67ace-121">-Policy</span></span>
<span data-ttu-id="67ace-122">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="67ace-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="67ace-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="67ace-123">-StartTime</span></span>
<span data-ttu-id="67ace-124">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="67ace-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="67ace-125">-Таблица</span><span class="sxs-lookup"><span data-stu-id="67ace-125">-Table</span></span>
<span data-ttu-id="67ace-126">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="67ace-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="67ace-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ace-127">CommonParameters</span></span>
<span data-ttu-id="67ace-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67ace-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ace-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67ace-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ace-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67ace-130">INPUTS</span></span>

### <span data-ttu-id="67ace-131">System. String</span><span class="sxs-lookup"><span data-stu-id="67ace-131">System.String</span></span>

### <span data-ttu-id="67ace-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="67ace-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="67ace-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67ace-133">OUTPUTS</span></span>

### <span data-ttu-id="67ace-134">System. String</span><span class="sxs-lookup"><span data-stu-id="67ace-134">System.String</span></span>

## <span data-ttu-id="67ace-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="67ace-135">NOTES</span></span>

## <span data-ttu-id="67ace-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67ace-136">RELATED LINKS</span></span>

[<span data-ttu-id="67ace-137">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="67ace-137">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="67ace-138">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="67ace-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="67ace-139">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="67ace-139">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="67ace-140">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="67ace-140">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


