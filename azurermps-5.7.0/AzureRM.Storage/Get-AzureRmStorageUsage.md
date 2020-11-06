---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
ms.openlocfilehash: 5d44fa0a3e0ead373a822ae91080df9bdc60cc50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567371"
---
# <span data-ttu-id="19878-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="19878-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="19878-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19878-102">SYNOPSIS</span></span>
<span data-ttu-id="19878-103">Получает использование ресурса хранилища для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="19878-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19878-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19878-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19878-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19878-105">DESCRIPTION</span></span>
<span data-ttu-id="19878-106">Командлет **Get-AzureRmStorageUsage** получает сведения об использовании ресурсов службой хранилища Azure для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="19878-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="19878-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19878-107">EXAMPLES</span></span>

### <span data-ttu-id="19878-108">Пример 1: получение сведений об использовании ресурсов хранилища</span><span class="sxs-lookup"><span data-stu-id="19878-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="19878-109">Эта команда получает использование ресурсов хранилища для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="19878-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="19878-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19878-110">PARAMETERS</span></span>

### <span data-ttu-id="19878-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19878-111">-DefaultProfile</span></span>
<span data-ttu-id="19878-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19878-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19878-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19878-113">CommonParameters</span></span>
<span data-ttu-id="19878-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19878-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19878-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19878-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19878-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19878-116">INPUTS</span></span>

### <span data-ttu-id="19878-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="19878-117">None</span></span>
<span data-ttu-id="19878-118">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="19878-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19878-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19878-119">OUTPUTS</span></span>

### <span data-ttu-id="19878-120">Microsoft. Azure. Commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="19878-120">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="19878-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="19878-121">NOTES</span></span>

## <span data-ttu-id="19878-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19878-122">RELATED LINKS</span></span>

[<span data-ttu-id="19878-123">Командлеты диспетчера хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="19878-123">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


