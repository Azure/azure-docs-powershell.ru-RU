---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 247b0735e41f02a55b94e5a8f8ed44136eb3f37e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559552"
---
# <span data-ttu-id="ad0af-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ad0af-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="ad0af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad0af-102">SYNOPSIS</span></span>
<span data-ttu-id="ad0af-103">Извлекает список учетных данных, связанных с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="ad0af-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad0af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad0af-104">SYNTAX</span></span>

### <span data-ttu-id="ad0af-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad0af-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad0af-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad0af-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad0af-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad0af-107">DESCRIPTION</span></span>
<span data-ttu-id="ad0af-108">Для получения списка учетных данных, связанных с субъектом-службой, можно использовать командлет Get-AzureRmADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="ad0af-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="ad0af-109">Эта команда извлекает все свойства учетных данных (но не значение учетных данных), связанные с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="ad0af-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="ad0af-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad0af-110">EXAMPLES</span></span>

### <span data-ttu-id="ad0af-111">--------------------------Пример 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ad0af-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="ad0af-112">Возвращает список учетных данных, связанных с субъектом-службой, имеющим имя участника-службы " http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="ad0af-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="ad0af-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad0af-113">PARAMETERS</span></span>

### <span data-ttu-id="ad0af-114">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ad0af-114">-ObjectId</span></span>
<span data-ttu-id="ad0af-115">Идентификатор объекта субъекта-службы, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="ad0af-115">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad0af-116">-Намерено</span><span class="sxs-lookup"><span data-stu-id="ad0af-116">-ServicePrincipalName</span></span>
<span data-ttu-id="ad0af-117">Имя (SPN) субъекта-службы, из которого нужно получить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="ad0af-117">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad0af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad0af-118">-DefaultProfile</span></span>
<span data-ttu-id="ad0af-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad0af-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad0af-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad0af-120">CommonParameters</span></span>
<span data-ttu-id="ad0af-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad0af-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad0af-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad0af-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad0af-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad0af-123">INPUTS</span></span>

## <span data-ttu-id="ad0af-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad0af-124">OUTPUTS</span></span>

### <span data-ttu-id="ad0af-125">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="ad0af-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="ad0af-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad0af-126">NOTES</span></span>

## <span data-ttu-id="ad0af-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad0af-127">RELATED LINKS</span></span>

[<span data-ttu-id="ad0af-128">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ad0af-128">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="ad0af-129">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ad0af-129">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="ad0af-130">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ad0af-130">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

