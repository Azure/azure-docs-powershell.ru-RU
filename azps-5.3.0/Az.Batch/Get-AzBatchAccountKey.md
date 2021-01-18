---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: 2662eeeeaedbac75f443bf6160c625dfdb8dd854
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509758"
---
# <span data-ttu-id="80e44-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="80e44-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="80e44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80e44-102">SYNOPSIS</span></span>
<span data-ttu-id="80e44-103">Ключи для пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="80e44-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="80e44-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="80e44-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80e44-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80e44-105">DESCRIPTION</span></span>
<span data-ttu-id="80e44-106">Для получения ключей учетной записи Azure Batch в текущей подписке возвращается ключ учетной записи **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="80e44-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="80e44-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="80e44-107">EXAMPLES</span></span>

### <span data-ttu-id="80e44-108">Пример 1. Получите ключи пакетной учетной записи и сохраните их в переменной $Context для использования в дальнейшем</span><span class="sxs-lookup"><span data-stu-id="80e44-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="80e44-109">Эта команда получает сведения об учетной записи и сохраняет их в `$Context` объекте для использования в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="80e44-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="80e44-110">Пример 2. Получить пакетные ключи учетной записи и отобразить их</span><span class="sxs-lookup"><span data-stu-id="80e44-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="80e44-111">Эта команда получает ключи учетной записи и печатает их на консоли.</span><span class="sxs-lookup"><span data-stu-id="80e44-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="80e44-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80e44-112">PARAMETERS</span></span>

### <span data-ttu-id="80e44-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="80e44-113">-AccountName</span></span>
<span data-ttu-id="80e44-114">Указывает имя учетной записи, для которой этот cmdlet получает ключи.</span><span class="sxs-lookup"><span data-stu-id="80e44-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80e44-115">-DefaultProfile</span></span>
<span data-ttu-id="80e44-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80e44-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e44-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80e44-117">-ResourceGroupName</span></span>
<span data-ttu-id="80e44-118">Указывает имя группы ресурсов, которая содержит учетную запись, для которой этот cmdlet получает ключи.</span><span class="sxs-lookup"><span data-stu-id="80e44-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e44-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e44-119">CommonParameters</span></span>
<span data-ttu-id="80e44-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80e44-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e44-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80e44-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e44-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80e44-122">INPUTS</span></span>

### <span data-ttu-id="80e44-123">System.String</span><span class="sxs-lookup"><span data-stu-id="80e44-123">System.String</span></span>

## <span data-ttu-id="80e44-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="80e44-124">OUTPUTS</span></span>

### <span data-ttu-id="80e44-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="80e44-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="80e44-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="80e44-126">NOTES</span></span>

## <span data-ttu-id="80e44-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80e44-127">RELATED LINKS</span></span>

[<span data-ttu-id="80e44-128">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="80e44-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="80e44-129">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="80e44-129">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
