---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b17a294392ca4336d4a96e5d136ad4e321eb45a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066747"
---
# <span data-ttu-id="12e4d-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="12e4d-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="12e4d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="12e4d-103">Возвращает политику и политики для сохраненной или политики доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="12e4d-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="12e4d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12e4d-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12e4d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12e4d-105">DESCRIPTION</span></span>
<span data-ttu-id="12e4d-106">Командлет **Get-AzStorageTableStoredAccessPolicy** включает в себя политику и политики для таблицы хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="12e4d-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="12e4d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12e4d-107">EXAMPLES</span></span>

### <span data-ttu-id="12e4d-108">Пример 1: получение политики доступа на хранение в таблице хранилища</span><span class="sxs-lookup"><span data-stu-id="12e4d-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="12e4d-109">Эта команда получает политику доступа с именем Policy50 в таблице хранения данных с именем Table02.</span><span class="sxs-lookup"><span data-stu-id="12e4d-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="12e4d-110">Пример 2: получение всех сохраненных политик доступа в таблице хранилища</span><span class="sxs-lookup"><span data-stu-id="12e4d-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="12e4d-111">Эта команда получает все политики доступа в таблице с именем Table02.</span><span class="sxs-lookup"><span data-stu-id="12e4d-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="12e4d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12e4d-112">PARAMETERS</span></span>

### <span data-ttu-id="12e4d-113">-Context</span><span class="sxs-lookup"><span data-stu-id="12e4d-113">-Context</span></span>
<span data-ttu-id="12e4d-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="12e4d-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="12e4d-115">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="12e4d-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="12e4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e4d-116">-DefaultProfile</span></span>
<span data-ttu-id="12e4d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12e4d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e4d-118">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="12e4d-118">-Policy</span></span>
<span data-ttu-id="12e4d-119">Указывает политику сохраненного доступа, которая включает разрешения для маркера данной подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="12e4d-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="12e4d-120">-Таблица</span><span class="sxs-lookup"><span data-stu-id="12e4d-120">-Table</span></span>
<span data-ttu-id="12e4d-121">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="12e4d-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="12e4d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e4d-122">CommonParameters</span></span>
<span data-ttu-id="12e4d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12e4d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e4d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12e4d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e4d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12e4d-125">INPUTS</span></span>

### <span data-ttu-id="12e4d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="12e4d-126">System.String</span></span>

### <span data-ttu-id="12e4d-127">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="12e4d-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="12e4d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12e4d-128">OUTPUTS</span></span>

### <span data-ttu-id="12e4d-129">Microsoft. WindowsAzure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="12e4d-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="12e4d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="12e4d-130">NOTES</span></span>

## <span data-ttu-id="12e4d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12e4d-131">RELATED LINKS</span></span>

[<span data-ttu-id="12e4d-132">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="12e4d-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="12e4d-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="12e4d-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="12e4d-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="12e4d-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="12e4d-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="12e4d-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


