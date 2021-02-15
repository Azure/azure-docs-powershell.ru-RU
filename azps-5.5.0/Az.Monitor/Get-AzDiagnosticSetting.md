---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: d1a6859638bfbcb69e479f4bc18a6a36c8aa68fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214252"
---
# <span data-ttu-id="5fc0c-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="5fc0c-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="5fc0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fc0c-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc0c-103">Возвращает категории и время, занося в журнал.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="5fc0c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5fc0c-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fc0c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fc0c-105">DESCRIPTION</span></span>
<span data-ttu-id="5fc0c-106">С **его учетом** можно получить категории и время, которые регистрируются для ресурса.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="5fc0c-107">Временная единица — это интервал агрегирования метрик.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="5fc0c-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5fc0c-108">EXAMPLES</span></span>

### <span data-ttu-id="5fc0c-109">Пример 1. Просмотр состояния категорий ведения журнала и временная заготовка</span><span class="sxs-lookup"><span data-stu-id="5fc0c-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="5fc0c-110">Эта команда возвращает категории и значения времени, которые регистрируются для  хранилища ключей Azure с ид/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="5fc0c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fc0c-111">PARAMETERS</span></span>

### <span data-ttu-id="5fc0c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc0c-112">-DefaultProfile</span></span>
<span data-ttu-id="5fc0c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5fc0c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fc0c-114">-Name</span><span class="sxs-lookup"><span data-stu-id="5fc0c-114">-Name</span></span>
<span data-ttu-id="5fc0c-115">Имя параметра диагностики.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="5fc0c-116">Если не дан вызов по умолчанию службе, как в предыдущем API.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="5fc0c-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fc0c-117">-ResourceId</span></span>
<span data-ttu-id="5fc0c-118">Определяет ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="5fc0c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc0c-119">CommonParameters</span></span>
<span data-ttu-id="5fc0c-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc0c-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fc0c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc0c-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fc0c-122">INPUTS</span></span>

### <span data-ttu-id="5fc0c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="5fc0c-123">System.String</span></span>

## <span data-ttu-id="5fc0c-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5fc0c-124">OUTPUTS</span></span>

### <span data-ttu-id="5fc0c-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="5fc0c-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="5fc0c-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5fc0c-126">NOTES</span></span>

## <span data-ttu-id="5fc0c-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fc0c-127">RELATED LINKS</span></span>

<span data-ttu-id="5fc0c-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="5fc0c-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
