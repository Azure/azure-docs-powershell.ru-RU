---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: fa2368e1982e66d8edecc465d1f6ded3a3d75205
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563332"
---
# <span data-ttu-id="7988d-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7988d-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="7988d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7988d-102">SYNOPSIS</span></span>
<span data-ttu-id="7988d-103">Извлекает список учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="7988d-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7988d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7988d-104">SYNTAX</span></span>

### <span data-ttu-id="7988d-105">ApplicationObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7988d-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7988d-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7988d-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7988d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7988d-107">DESCRIPTION</span></span>
<span data-ttu-id="7988d-108">Командлет Get-AzureRmADAppCredential можно использовать для получения списка учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="7988d-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="7988d-109">Эта команда извлекает все свойства учетных данных (но не значение учетных данных), связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="7988d-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="7988d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7988d-110">EXAMPLES</span></span>

### <span data-ttu-id="7988d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7988d-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="7988d-112">Возвращает список учетных данных, связанных с приложением с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="7988d-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="7988d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7988d-113">PARAMETERS</span></span>

### <span data-ttu-id="7988d-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7988d-114">-ApplicationId</span></span>
<span data-ttu-id="7988d-115">Идентификатор приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="7988d-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7988d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7988d-116">-DefaultProfile</span></span>
<span data-ttu-id="7988d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7988d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7988d-118">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7988d-118">-ObjectId</span></span>
<span data-ttu-id="7988d-119">Идентификатор объекта приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="7988d-119">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7988d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7988d-120">CommonParameters</span></span>
<span data-ttu-id="7988d-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7988d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7988d-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7988d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7988d-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7988d-123">INPUTS</span></span>

### <span data-ttu-id="7988d-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="7988d-124">None</span></span>
<span data-ttu-id="7988d-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7988d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7988d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7988d-126">OUTPUTS</span></span>

### <span data-ttu-id="7988d-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="7988d-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="7988d-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="7988d-128">NOTES</span></span>

## <span data-ttu-id="7988d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7988d-129">RELATED LINKS</span></span>

[<span data-ttu-id="7988d-130">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7988d-130">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="7988d-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7988d-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="7988d-132">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7988d-132">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

