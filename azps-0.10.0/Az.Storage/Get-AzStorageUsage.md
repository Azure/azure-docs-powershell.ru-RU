---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: edf78ad4022b29251d78e976ff7e5d66ae67bb69
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910743"
---
# <span data-ttu-id="acf4b-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="acf4b-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="acf4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="acf4b-102">SYNOPSIS</span></span>
<span data-ttu-id="acf4b-103">Получает использование ресурса хранилища для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="acf4b-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="acf4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="acf4b-104">SYNTAX</span></span>

```
Get-AzStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acf4b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acf4b-105">DESCRIPTION</span></span>
<span data-ttu-id="acf4b-106">Командлет **Get-AzStorageUsage** получает сведения об использовании ресурсов службой хранилища Azure для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="acf4b-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="acf4b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="acf4b-107">EXAMPLES</span></span>

### <span data-ttu-id="acf4b-108">Пример 1: получение сведений об использовании ресурсов хранилища</span><span class="sxs-lookup"><span data-stu-id="acf4b-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzStorageUsage
```

<span data-ttu-id="acf4b-109">Эта команда получает использование ресурсов хранилища для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="acf4b-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="acf4b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="acf4b-110">PARAMETERS</span></span>

### <span data-ttu-id="acf4b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf4b-111">-DefaultProfile</span></span>
<span data-ttu-id="acf4b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acf4b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf4b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf4b-113">CommonParameters</span></span>
<span data-ttu-id="acf4b-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="acf4b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf4b-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acf4b-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf4b-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="acf4b-116">INPUTS</span></span>

### <span data-ttu-id="acf4b-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="acf4b-117">None</span></span>

## <span data-ttu-id="acf4b-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="acf4b-118">OUTPUTS</span></span>

### <span data-ttu-id="acf4b-119">Microsoft. Azure. Commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="acf4b-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="acf4b-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="acf4b-120">NOTES</span></span>

## <span data-ttu-id="acf4b-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acf4b-121">RELATED LINKS</span></span>

[<span data-ttu-id="acf4b-122">Командлеты диспетчера хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="acf4b-122">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


