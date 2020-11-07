---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 236ce405c222ba3b7746ba1affca8f288045f8a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733733"
---
# <span data-ttu-id="8e5b2-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8e5b2-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="8e5b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e5b2-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5b2-103">Получает записанные в журнал временные Гранки и категории.</span><span class="sxs-lookup"><span data-stu-id="8e5b2-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e5b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e5b2-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e5b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e5b2-105">DESCRIPTION</span></span>
<span data-ttu-id="8e5b2-106">Командлет **Get-AzureRmDiagnosticSetting** получает категории и временные грани, которые регистрируются для ресурса.</span><span class="sxs-lookup"><span data-stu-id="8e5b2-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>

<span data-ttu-id="8e5b2-107">Промежуток времени — это интервал агрегирования метрики.</span><span class="sxs-lookup"><span data-stu-id="8e5b2-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="8e5b2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e5b2-108">EXAMPLES</span></span>

### <span data-ttu-id="8e5b2-109">Пример 1: получение состояния категорий ведения журнала и временных граней</span><span class="sxs-lookup"><span data-stu-id="8e5b2-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="8e5b2-110">Эта команда получает категории и временные Гранки, которые были зарегистрированы для хранилища ключей Azure с *ResourceId* для/Subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="8e5b2-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="8e5b2-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e5b2-111">PARAMETERS</span></span>

### <span data-ttu-id="8e5b2-112">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e5b2-112">-ResourceId</span></span>
<span data-ttu-id="8e5b2-113">Указывает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8e5b2-113">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e5b2-114">-DefaultProfile</span></span>
<span data-ttu-id="8e5b2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e5b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e5b2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5b2-116">CommonParameters</span></span>
<span data-ttu-id="8e5b2-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e5b2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5b2-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e5b2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5b2-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e5b2-119">INPUTS</span></span>

## <span data-ttu-id="8e5b2-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e5b2-120">OUTPUTS</span></span>

### <span data-ttu-id="8e5b2-121">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="8e5b2-121">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="8e5b2-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e5b2-122">NOTES</span></span>

## <span data-ttu-id="8e5b2-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e5b2-123">RELATED LINKS</span></span>

[<span data-ttu-id="8e5b2-124">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8e5b2-124">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


