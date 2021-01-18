---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b17a294392ca4336d4a96e5d136ad4e321eb45a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504660"
---
# <span data-ttu-id="3176b-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3176b-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="3176b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3176b-102">SYNOPSIS</span></span>
<span data-ttu-id="3176b-103">Возвращает хранимую политику или политики доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3176b-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="3176b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3176b-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3176b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3176b-105">DESCRIPTION</span></span>
<span data-ttu-id="3176b-106">В **этом списке** указаны политики или политики доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3176b-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="3176b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3176b-107">EXAMPLES</span></span>

### <span data-ttu-id="3176b-108">Пример 1. Хранение политики доступа в таблице хранилища</span><span class="sxs-lookup"><span data-stu-id="3176b-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="3176b-109">Эта команда получает политику доступа "Политика50" в таблице хранилища Table02.</span><span class="sxs-lookup"><span data-stu-id="3176b-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="3176b-110">Пример 2. Все хранимые политики доступа в таблице хранения</span><span class="sxs-lookup"><span data-stu-id="3176b-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="3176b-111">Эта команда получает все политики доступа в таблице Table02.</span><span class="sxs-lookup"><span data-stu-id="3176b-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="3176b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3176b-112">PARAMETERS</span></span>

### <span data-ttu-id="3176b-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="3176b-113">-Context</span></span>
<span data-ttu-id="3176b-114">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3176b-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3176b-115">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="3176b-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3176b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3176b-116">-DefaultProfile</span></span>
<span data-ttu-id="3176b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3176b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3176b-118">-Политика</span><span class="sxs-lookup"><span data-stu-id="3176b-118">-Policy</span></span>
<span data-ttu-id="3176b-119">Определяет хранимую политику доступа, которая включает разрешения для этого маркера подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="3176b-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="3176b-120">-Table</span><span class="sxs-lookup"><span data-stu-id="3176b-120">-Table</span></span>
<span data-ttu-id="3176b-121">Имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3176b-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="3176b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3176b-122">CommonParameters</span></span>
<span data-ttu-id="3176b-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3176b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3176b-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3176b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3176b-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3176b-125">INPUTS</span></span>

### <span data-ttu-id="3176b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="3176b-126">System.String</span></span>

### <span data-ttu-id="3176b-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3176b-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3176b-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3176b-128">OUTPUTS</span></span>

### <span data-ttu-id="3176b-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="3176b-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="3176b-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3176b-130">NOTES</span></span>

## <span data-ttu-id="3176b-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3176b-131">RELATED LINKS</span></span>

[<span data-ttu-id="3176b-132">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3176b-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3176b-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3176b-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3176b-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3176b-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3176b-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3176b-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


