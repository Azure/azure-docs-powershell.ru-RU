---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: a9289bc6a0db4403b96e982fd28f91578e3a0c9b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913157"
---
# <span data-ttu-id="001fe-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="001fe-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="001fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="001fe-102">SYNOPSIS</span></span>
<span data-ttu-id="001fe-103">Возвращает ключи учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="001fe-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="001fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="001fe-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="001fe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="001fe-105">DESCRIPTION</span></span>
<span data-ttu-id="001fe-106">Командлет **Get-AzBatchAccountKey** получает ключи учетной записи пакетной службы Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="001fe-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="001fe-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="001fe-107">EXAMPLES</span></span>

### <span data-ttu-id="001fe-108">Пример 1: получение ключей учетной записи пакета и сохранение их в $Context переменной для использования в будущем</span><span class="sxs-lookup"><span data-stu-id="001fe-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="001fe-109">Эта команда возвращает данные учетной записи и сохраняет ее в `$Context` объекте для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="001fe-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="001fe-110">Пример 2: получение ключей учетной записи пакета и их отображение</span><span class="sxs-lookup"><span data-stu-id="001fe-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="001fe-111">Эта команда получает ключи учетной записи и печатает их на консоли.</span><span class="sxs-lookup"><span data-stu-id="001fe-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="001fe-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="001fe-112">PARAMETERS</span></span>

### <span data-ttu-id="001fe-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="001fe-113">-AccountName</span></span>
<span data-ttu-id="001fe-114">Указывает имя учетной записи, для которой этот командлет получает ключи.</span><span class="sxs-lookup"><span data-stu-id="001fe-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="001fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="001fe-115">-DefaultProfile</span></span>
<span data-ttu-id="001fe-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="001fe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="001fe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="001fe-117">-ResourceGroupName</span></span>
<span data-ttu-id="001fe-118">Указывает имя группы ресурсов, которая содержит учетную запись, для которой этот командлет получает ключи.</span><span class="sxs-lookup"><span data-stu-id="001fe-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="001fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="001fe-119">CommonParameters</span></span>
<span data-ttu-id="001fe-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="001fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="001fe-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="001fe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="001fe-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="001fe-122">INPUTS</span></span>

### <span data-ttu-id="001fe-123">System. String</span><span class="sxs-lookup"><span data-stu-id="001fe-123">System.String</span></span>

## <span data-ttu-id="001fe-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="001fe-124">OUTPUTS</span></span>

### <span data-ttu-id="001fe-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="001fe-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="001fe-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="001fe-126">NOTES</span></span>

## <span data-ttu-id="001fe-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="001fe-127">RELATED LINKS</span></span>

[<span data-ttu-id="001fe-128">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="001fe-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="001fe-129">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="001fe-129">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


