---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 82e5d252e2e8185b98c142b24537c666e5618d7f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324648"
---
# <span data-ttu-id="4210a-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4210a-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="4210a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4210a-102">SYNOPSIS</span></span>
<span data-ttu-id="4210a-103">Создает политику хранимого доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4210a-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="4210a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4210a-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4210a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4210a-105">DESCRIPTION</span></span>
<span data-ttu-id="4210a-106">Для таблицы хранилища Azure создается политика доступа **New-AzStorageTableStoredAccessPolicy.**</span><span class="sxs-lookup"><span data-stu-id="4210a-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="4210a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4210a-107">EXAMPLES</span></span>

### <span data-ttu-id="4210a-108">Пример 1. Создание политики хранимого доступа в таблице</span><span class="sxs-lookup"><span data-stu-id="4210a-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="4210a-109">Эта команда создает политику доступа с именем "Политика02" в таблице хранилища "Моятаблицы".</span><span class="sxs-lookup"><span data-stu-id="4210a-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="4210a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4210a-110">PARAMETERS</span></span>

### <span data-ttu-id="4210a-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="4210a-111">-Context</span></span>
<span data-ttu-id="4210a-112">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4210a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4210a-113">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="4210a-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4210a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4210a-114">-DefaultProfile</span></span>
<span data-ttu-id="4210a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4210a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4210a-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4210a-116">-ExpiryTime</span></span>
<span data-ttu-id="4210a-117">Время, в течение которого хранимая политика доступа становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="4210a-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="4210a-118">-Permission</span><span class="sxs-lookup"><span data-stu-id="4210a-118">-Permission</span></span>
<span data-ttu-id="4210a-119">Определяет разрешения в хранимой политике доступа на доступ к таблице хранения.</span><span class="sxs-lookup"><span data-stu-id="4210a-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="4210a-120">Важно отметить, что это строка (для чтения, записи `rwd` и удаления).</span><span class="sxs-lookup"><span data-stu-id="4210a-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="4210a-121">-Политика</span><span class="sxs-lookup"><span data-stu-id="4210a-121">-Policy</span></span>
<span data-ttu-id="4210a-122">Указывает имя хранимой политики доступа.</span><span class="sxs-lookup"><span data-stu-id="4210a-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="4210a-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4210a-123">-StartTime</span></span>
<span data-ttu-id="4210a-124">Время, в течение которого хранимая политика доступа становится допустимой.</span><span class="sxs-lookup"><span data-stu-id="4210a-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="4210a-125">-Table</span><span class="sxs-lookup"><span data-stu-id="4210a-125">-Table</span></span>
<span data-ttu-id="4210a-126">Имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4210a-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="4210a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4210a-127">CommonParameters</span></span>
<span data-ttu-id="4210a-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4210a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4210a-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4210a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4210a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4210a-130">INPUTS</span></span>

### <span data-ttu-id="4210a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4210a-131">System.String</span></span>

### <span data-ttu-id="4210a-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4210a-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4210a-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4210a-133">OUTPUTS</span></span>

### <span data-ttu-id="4210a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4210a-134">System.String</span></span>

## <span data-ttu-id="4210a-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4210a-135">NOTES</span></span>

## <span data-ttu-id="4210a-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4210a-136">RELATED LINKS</span></span>

[<span data-ttu-id="4210a-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4210a-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4210a-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4210a-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4210a-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4210a-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4210a-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4210a-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


