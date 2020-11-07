---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: a9c141684eb924ed0b969c469214d92b847e13db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914306"
---
# <span data-ttu-id="7c762-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7c762-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="7c762-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c762-102">SYNOPSIS</span></span>
<span data-ttu-id="7c762-103">Возвращает политику и политики для сохраненной или политики доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7c762-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c762-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c762-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c762-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c762-105">DESCRIPTION</span></span>
<span data-ttu-id="7c762-106">Командлет **Get-AzureStorageTableStoredAccessPolicy** включает в себя политику и политики для таблицы хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="7c762-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="7c762-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c762-107">EXAMPLES</span></span>

### <span data-ttu-id="7c762-108">Пример 1: получение политики доступа на хранение в таблице хранилища</span><span class="sxs-lookup"><span data-stu-id="7c762-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="7c762-109">Эта команда получает политику доступа с именем Policy50 в таблице хранения данных с именем Table02.</span><span class="sxs-lookup"><span data-stu-id="7c762-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="7c762-110">Пример 2: получение всех сохраненных политик доступа в таблице хранилища</span><span class="sxs-lookup"><span data-stu-id="7c762-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="7c762-111">Эта команда получает все политики доступа в таблице с именем Table02.</span><span class="sxs-lookup"><span data-stu-id="7c762-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="7c762-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c762-112">PARAMETERS</span></span>

### <span data-ttu-id="7c762-113">-Context</span><span class="sxs-lookup"><span data-stu-id="7c762-113">-Context</span></span>
<span data-ttu-id="7c762-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7c762-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="7c762-115">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7c762-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7c762-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c762-116">-DefaultProfile</span></span>
<span data-ttu-id="7c762-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c762-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c762-118">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="7c762-118">-Policy</span></span>
<span data-ttu-id="7c762-119">Указывает политику сохраненного доступа, которая включает разрешения для маркера данной подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="7c762-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c762-120">-Таблица</span><span class="sxs-lookup"><span data-stu-id="7c762-120">-Table</span></span>
<span data-ttu-id="7c762-121">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7c762-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="7c762-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c762-122">CommonParameters</span></span>
<span data-ttu-id="7c762-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c762-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c762-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c762-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c762-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c762-125">INPUTS</span></span>

### <span data-ttu-id="7c762-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7c762-126">System.String</span></span>

### <span data-ttu-id="7c762-127">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7c762-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7c762-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c762-128">OUTPUTS</span></span>

### <span data-ttu-id="7c762-129">Microsoft. WindowsAzure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="7c762-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="7c762-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c762-130">NOTES</span></span>

## <span data-ttu-id="7c762-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c762-131">RELATED LINKS</span></span>

[<span data-ttu-id="7c762-132">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7c762-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7c762-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7c762-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7c762-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7c762-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7c762-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7c762-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


