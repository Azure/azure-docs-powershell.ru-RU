---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: d1a6859638bfbcb69e479f4bc18a6a36c8aa68fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074089"
---
# <span data-ttu-id="37054-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="37054-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="37054-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37054-102">SYNOPSIS</span></span>
<span data-ttu-id="37054-103">Получает записанные в журнал временные Гранки и категории.</span><span class="sxs-lookup"><span data-stu-id="37054-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="37054-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37054-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37054-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37054-105">DESCRIPTION</span></span>
<span data-ttu-id="37054-106">Командлет **Get-AzDiagnosticSetting** получает категории и временные грани, которые регистрируются для ресурса.</span><span class="sxs-lookup"><span data-stu-id="37054-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="37054-107">Промежуток времени — это интервал агрегирования метрики.</span><span class="sxs-lookup"><span data-stu-id="37054-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="37054-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37054-108">EXAMPLES</span></span>

### <span data-ttu-id="37054-109">Пример 1: получение состояния категорий ведения журнала и временных граней</span><span class="sxs-lookup"><span data-stu-id="37054-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="37054-110">Эта команда получает категории и временные Гранки, которые были зарегистрированы для хранилища ключей Azure с *ResourceId* для/Subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="37054-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="37054-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37054-111">PARAMETERS</span></span>

### <span data-ttu-id="37054-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37054-112">-DefaultProfile</span></span>
<span data-ttu-id="37054-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="37054-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37054-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="37054-114">-Name</span></span>
<span data-ttu-id="37054-115">Имя параметра диагностики.</span><span class="sxs-lookup"><span data-stu-id="37054-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="37054-116">Если не задано значение по умолчанию для вызова "Service", так как оно находится в предыдущем API.</span><span class="sxs-lookup"><span data-stu-id="37054-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="37054-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37054-117">-ResourceId</span></span>
<span data-ttu-id="37054-118">Указывает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="37054-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="37054-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37054-119">CommonParameters</span></span>
<span data-ttu-id="37054-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37054-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37054-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37054-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37054-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37054-122">INPUTS</span></span>

### <span data-ttu-id="37054-123">System. String</span><span class="sxs-lookup"><span data-stu-id="37054-123">System.String</span></span>

## <span data-ttu-id="37054-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37054-124">OUTPUTS</span></span>

### <span data-ttu-id="37054-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="37054-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="37054-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="37054-126">NOTES</span></span>

## <span data-ttu-id="37054-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37054-127">RELATED LINKS</span></span>

<span data-ttu-id="37054-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="37054-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
