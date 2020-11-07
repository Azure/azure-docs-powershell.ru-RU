---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 6bab9613a2b109ef0cd8d0d65bf2fb770d91eb16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734082"
---
# <span data-ttu-id="6a403-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6a403-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="6a403-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a403-102">SYNOPSIS</span></span>
<span data-ttu-id="6a403-103">Возвращает ключи учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="6a403-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a403-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a403-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a403-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a403-105">DESCRIPTION</span></span>
<span data-ttu-id="6a403-106">Командлет **Get-AzureRmBatchAccountKeys** получает ключи учетной записи пакетной службы Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="6a403-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="6a403-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a403-107">EXAMPLES</span></span>

## <span data-ttu-id="6a403-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a403-108">PARAMETERS</span></span>

### <span data-ttu-id="6a403-109">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="6a403-109">-AccountName</span></span>
<span data-ttu-id="6a403-110">Указывает имя учетной записи, для которой этот командлет получает ключи.</span><span class="sxs-lookup"><span data-stu-id="6a403-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="6a403-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a403-111">-ResourceGroupName</span></span>
<span data-ttu-id="6a403-112">Указывает имя группы ресурсов, которая содержит учетную запись, для которой этот командлет получает ключи.</span><span class="sxs-lookup"><span data-stu-id="6a403-112">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="6a403-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a403-113">-DefaultProfile</span></span>
<span data-ttu-id="6a403-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a403-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a403-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a403-115">CommonParameters</span></span>
<span data-ttu-id="6a403-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a403-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a403-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a403-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a403-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a403-118">INPUTS</span></span>

## <span data-ttu-id="6a403-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a403-119">OUTPUTS</span></span>

### <span data-ttu-id="6a403-120">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6a403-120">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6a403-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a403-121">NOTES</span></span>

## <span data-ttu-id="6a403-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a403-122">RELATED LINKS</span></span>

[<span data-ttu-id="6a403-123">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6a403-123">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="6a403-124">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="6a403-124">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


