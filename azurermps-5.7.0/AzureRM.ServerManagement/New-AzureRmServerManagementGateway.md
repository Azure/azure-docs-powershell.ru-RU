---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: f73d53fc3031fc72be950547e5b9c2b93a9a0079
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732358"
---
# <span data-ttu-id="acb20-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="acb20-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="acb20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="acb20-102">SYNOPSIS</span></span>
<span data-ttu-id="acb20-103">Создание шлюза управления сервером.</span><span class="sxs-lookup"><span data-stu-id="acb20-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acb20-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="acb20-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acb20-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acb20-105">DESCRIPTION</span></span>
<span data-ttu-id="acb20-106">Командлет **New-AzureRmServerManagementGateway** создает шлюз управления сервером Azure.</span><span class="sxs-lookup"><span data-stu-id="acb20-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="acb20-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="acb20-107">EXAMPLES</span></span>

## <span data-ttu-id="acb20-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="acb20-108">PARAMETERS</span></span>

### <span data-ttu-id="acb20-109">-Автоматическое обновление</span><span class="sxs-lookup"><span data-stu-id="acb20-109">-AutoUpgrade</span></span>
<span data-ttu-id="acb20-110">Указывает на то, что шлюз будет автоматически обновляться при выпуске новой версии.</span><span class="sxs-lookup"><span data-stu-id="acb20-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acb20-111">-DefaultProfile</span></span>
<span data-ttu-id="acb20-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acb20-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acb20-113">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="acb20-113">-GatewayName</span></span>
<span data-ttu-id="acb20-114">Указывает имя шлюза, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="acb20-114">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb20-115">-Location</span><span class="sxs-lookup"><span data-stu-id="acb20-115">-Location</span></span>
<span data-ttu-id="acb20-116">Задает расположение, в котором нужно создать шлюз.</span><span class="sxs-lookup"><span data-stu-id="acb20-116">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb20-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acb20-117">-ResourceGroupName</span></span>
<span data-ttu-id="acb20-118">Указывает имя группы ресурсов, в которой этот командлет создает шлюз.</span><span class="sxs-lookup"><span data-stu-id="acb20-118">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb20-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="acb20-119">-Tag</span></span>
<span data-ttu-id="acb20-120">Пары "ключ-значение", связанные с шлюзом.</span><span class="sxs-lookup"><span data-stu-id="acb20-120">Key/value pairs associated with the gateway.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb20-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acb20-121">CommonParameters</span></span>
<span data-ttu-id="acb20-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="acb20-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acb20-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acb20-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acb20-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="acb20-124">INPUTS</span></span>

### <span data-ttu-id="acb20-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="acb20-125">None</span></span>
<span data-ttu-id="acb20-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="acb20-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="acb20-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="acb20-127">OUTPUTS</span></span>

### <span data-ttu-id="acb20-128">Microsoft. Azure. Commands. ServerManagement. Model. Gateway</span><span class="sxs-lookup"><span data-stu-id="acb20-128">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="acb20-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="acb20-129">NOTES</span></span>

## <span data-ttu-id="acb20-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acb20-130">RELATED LINKS</span></span>

[<span data-ttu-id="acb20-131">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="acb20-131">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="acb20-132">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="acb20-132">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


