---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 2b70fd58bd0b51e03079b1c24665b67ac3ad3a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564452"
---
# <span data-ttu-id="4e416-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="4e416-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="4e416-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e416-102">SYNOPSIS</span></span>
<span data-ttu-id="4e416-103">Получает записанные в журнал временные Гранки и категории.</span><span class="sxs-lookup"><span data-stu-id="4e416-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e416-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e416-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e416-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e416-105">DESCRIPTION</span></span>
<span data-ttu-id="4e416-106">Командлет **Get-AzureRmDiagnosticSetting** получает категории и временные грани, которые регистрируются для ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e416-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="4e416-107">Промежуток времени — это интервал агрегирования метрики.</span><span class="sxs-lookup"><span data-stu-id="4e416-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="4e416-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e416-108">EXAMPLES</span></span>

### <span data-ttu-id="4e416-109">Пример 1: получение состояния категорий ведения журнала и временных граней</span><span class="sxs-lookup"><span data-stu-id="4e416-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="4e416-110">Эта команда получает категории и временные Гранки, которые были зарегистрированы для хранилища ключей Azure с *ResourceId* для/Subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="4e416-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="4e416-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e416-111">PARAMETERS</span></span>

### <span data-ttu-id="4e416-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e416-112">-DefaultProfile</span></span>
<span data-ttu-id="4e416-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4e416-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e416-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e416-114">-Name</span></span>
<span data-ttu-id="4e416-115">Имя параметра диагностики.</span><span class="sxs-lookup"><span data-stu-id="4e416-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="4e416-116">Если не задано значение по умолчанию для вызова "Service", так как оно находится в предыдущем API.</span><span class="sxs-lookup"><span data-stu-id="4e416-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="4e416-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e416-117">-ResourceId</span></span>
<span data-ttu-id="4e416-118">Указывает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e416-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="4e416-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e416-119">CommonParameters</span></span>
<span data-ttu-id="4e416-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e416-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e416-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e416-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e416-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e416-122">INPUTS</span></span>

### <span data-ttu-id="4e416-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4e416-123">System.String</span></span>

## <span data-ttu-id="4e416-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e416-124">OUTPUTS</span></span>

### <span data-ttu-id="4e416-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="4e416-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="4e416-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e416-126">NOTES</span></span>

## <span data-ttu-id="4e416-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e416-127">RELATED LINKS</span></span>

<span data-ttu-id="4e416-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="4e416-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
