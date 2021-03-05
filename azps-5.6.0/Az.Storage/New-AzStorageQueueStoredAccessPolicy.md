---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f676f644cb69880a0b403a4e656ce9cb435b7c77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002387"
---
# <span data-ttu-id="eedba-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eedba-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="eedba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eedba-102">SYNOPSIS</span></span>
<span data-ttu-id="eedba-103">Создает политику хранимого доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="eedba-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="eedba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eedba-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eedba-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eedba-105">DESCRIPTION</span></span>
<span data-ttu-id="eedba-106">Для очереди хранения Azure создается политика доступа **New-AzStorageQueueStoredAccessPolicy.**</span><span class="sxs-lookup"><span data-stu-id="eedba-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="eedba-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eedba-107">EXAMPLES</span></span>

### <span data-ttu-id="eedba-108">Пример 1. Создание политики хранимого доступа в очереди хранилища</span><span class="sxs-lookup"><span data-stu-id="eedba-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="eedba-109">Эта команда создает политику доступа с именем Policy01 в очереди хранения MyQueue.</span><span class="sxs-lookup"><span data-stu-id="eedba-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="eedba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eedba-110">PARAMETERS</span></span>

### <span data-ttu-id="eedba-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="eedba-111">-Context</span></span>
<span data-ttu-id="eedba-112">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="eedba-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="eedba-113">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="eedba-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="eedba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eedba-114">-DefaultProfile</span></span>
<span data-ttu-id="eedba-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eedba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eedba-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="eedba-116">-ExpiryTime</span></span>
<span data-ttu-id="eedba-117">Определяет время, в течение которого хранимая политика доступа становится недопустимой.</span><span class="sxs-lookup"><span data-stu-id="eedba-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="eedba-118">-Permission</span><span class="sxs-lookup"><span data-stu-id="eedba-118">-Permission</span></span>
<span data-ttu-id="eedba-119">Определяет разрешения в хранимой политике доступа на доступ к очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="eedba-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="eedba-120">Важно отметить, что это строка (для `rwd` чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="eedba-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="eedba-121">-Политика</span><span class="sxs-lookup"><span data-stu-id="eedba-121">-Policy</span></span>
<span data-ttu-id="eedba-122">Указывает имя хранимой политики доступа.</span><span class="sxs-lookup"><span data-stu-id="eedba-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="eedba-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="eedba-123">-Queue</span></span>
<span data-ttu-id="eedba-124">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="eedba-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="eedba-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="eedba-125">-StartTime</span></span>
<span data-ttu-id="eedba-126">Время, в течение которого хранимая политика доступа становится допустимой.</span><span class="sxs-lookup"><span data-stu-id="eedba-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="eedba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eedba-127">CommonParameters</span></span>
<span data-ttu-id="eedba-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eedba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eedba-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eedba-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eedba-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eedba-130">INPUTS</span></span>

### <span data-ttu-id="eedba-131">System.String</span><span class="sxs-lookup"><span data-stu-id="eedba-131">System.String</span></span>

### <span data-ttu-id="eedba-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eedba-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eedba-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eedba-133">OUTPUTS</span></span>

### <span data-ttu-id="eedba-134">System.String</span><span class="sxs-lookup"><span data-stu-id="eedba-134">System.String</span></span>

## <span data-ttu-id="eedba-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eedba-135">NOTES</span></span>

## <span data-ttu-id="eedba-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eedba-136">RELATED LINKS</span></span>

[<span data-ttu-id="eedba-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eedba-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="eedba-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="eedba-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="eedba-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eedba-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="eedba-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eedba-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


