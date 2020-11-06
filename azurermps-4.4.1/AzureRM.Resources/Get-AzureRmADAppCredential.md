---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: e270a59e3799302eed49a0fd60180bb8d4589d92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569232"
---
# <span data-ttu-id="8d87c-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8d87c-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="8d87c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d87c-102">SYNOPSIS</span></span>
<span data-ttu-id="8d87c-103">Извлекает список учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="8d87c-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d87c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d87c-104">SYNTAX</span></span>

### <span data-ttu-id="8d87c-105">ApplicationObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d87c-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d87c-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d87c-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d87c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d87c-107">DESCRIPTION</span></span>
<span data-ttu-id="8d87c-108">Командлет Get-AzureRmADAppCredential можно использовать для получения списка учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="8d87c-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="8d87c-109">Эта команда извлекает все свойства учетных данных (но не значение учетных данных), связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="8d87c-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="8d87c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d87c-110">EXAMPLES</span></span>

### <span data-ttu-id="8d87c-111">--------------------------Пример 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8d87c-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="8d87c-112">Возвращает список учетных данных, связанных с приложением с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="8d87c-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="8d87c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d87c-113">PARAMETERS</span></span>

### <span data-ttu-id="8d87c-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8d87c-114">-ApplicationId</span></span>
<span data-ttu-id="8d87c-115">Идентификатор приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="8d87c-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d87c-116">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8d87c-116">-ObjectId</span></span>
<span data-ttu-id="8d87c-117">Идентификатор объекта приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="8d87c-117">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d87c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d87c-118">-DefaultProfile</span></span>
<span data-ttu-id="8d87c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d87c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d87c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d87c-120">CommonParameters</span></span>
<span data-ttu-id="8d87c-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d87c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d87c-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d87c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d87c-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d87c-123">INPUTS</span></span>

## <span data-ttu-id="8d87c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d87c-124">OUTPUTS</span></span>

### <span data-ttu-id="8d87c-125">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="8d87c-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="8d87c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d87c-126">NOTES</span></span>

## <span data-ttu-id="8d87c-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d87c-127">RELATED LINKS</span></span>

[<span data-ttu-id="8d87c-128">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8d87c-128">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="8d87c-129">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8d87c-129">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="8d87c-130">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="8d87c-130">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

