---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
ms.openlocfilehash: ae6524c46ed97563e7bf6c948f550a393d74f582
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913719"
---
# <span data-ttu-id="425bc-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="425bc-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="425bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="425bc-102">SYNOPSIS</span></span>
<span data-ttu-id="425bc-103">Получает использование ресурса хранилища для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="425bc-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="425bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="425bc-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="425bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="425bc-105">DESCRIPTION</span></span>
<span data-ttu-id="425bc-106">Командлет **Get-AzureRmStorageUsage** получает сведения об использовании ресурсов службой хранилища Azure для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="425bc-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="425bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="425bc-107">EXAMPLES</span></span>

### <span data-ttu-id="425bc-108">Пример 1: получение сведений об использовании ресурсов хранилища</span><span class="sxs-lookup"><span data-stu-id="425bc-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="425bc-109">Эта команда получает использование ресурсов хранилища для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="425bc-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="425bc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="425bc-110">PARAMETERS</span></span>

### <span data-ttu-id="425bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="425bc-111">-DefaultProfile</span></span>
<span data-ttu-id="425bc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="425bc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="425bc-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="425bc-113">CommonParameters</span></span>
<span data-ttu-id="425bc-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="425bc-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="425bc-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="425bc-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="425bc-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="425bc-116">INPUTS</span></span>

### <span data-ttu-id="425bc-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="425bc-117">None</span></span>

## <span data-ttu-id="425bc-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="425bc-118">OUTPUTS</span></span>

### <span data-ttu-id="425bc-119">Microsoft. Azure. Commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="425bc-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="425bc-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="425bc-120">NOTES</span></span>

## <span data-ttu-id="425bc-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="425bc-121">RELATED LINKS</span></span>

[<span data-ttu-id="425bc-122">Командлеты диспетчера хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="425bc-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


