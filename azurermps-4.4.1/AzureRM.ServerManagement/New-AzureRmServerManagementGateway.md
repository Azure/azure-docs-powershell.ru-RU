---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9cb98b9671f43ddd7acbcc84e8473a12da00f405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565140"
---
# <span data-ttu-id="a1d78-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a1d78-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="a1d78-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1d78-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d78-103">Создание шлюза управления сервером.</span><span class="sxs-lookup"><span data-stu-id="a1d78-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1d78-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1d78-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1d78-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1d78-105">DESCRIPTION</span></span>
<span data-ttu-id="a1d78-106">Командлет **New-AzureRmServerManagementGateway** создает шлюз управления сервером Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d78-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="a1d78-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1d78-107">EXAMPLES</span></span>

## <span data-ttu-id="a1d78-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1d78-108">PARAMETERS</span></span>

### <span data-ttu-id="a1d78-109">-Автоматическое обновление</span><span class="sxs-lookup"><span data-stu-id="a1d78-109">-AutoUpgrade</span></span>
<span data-ttu-id="a1d78-110">Указывает на то, что шлюз будет автоматически обновляться при выпуске новой версии.</span><span class="sxs-lookup"><span data-stu-id="a1d78-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d78-111">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="a1d78-111">-GatewayName</span></span>
<span data-ttu-id="a1d78-112">Указывает имя шлюза, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a1d78-112">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d78-113">-Location</span><span class="sxs-lookup"><span data-stu-id="a1d78-113">-Location</span></span>
<span data-ttu-id="a1d78-114">Задает расположение, в котором нужно создать шлюз.</span><span class="sxs-lookup"><span data-stu-id="a1d78-114">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d78-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d78-115">-ResourceGroupName</span></span>
<span data-ttu-id="a1d78-116">Указывает имя группы ресурсов, в которой этот командлет создает шлюз.</span><span class="sxs-lookup"><span data-stu-id="a1d78-116">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

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

### <span data-ttu-id="a1d78-117">-Теги</span><span class="sxs-lookup"><span data-stu-id="a1d78-117">-Tags</span></span>
<span data-ttu-id="a1d78-118">Определяет теги как пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="a1d78-118">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="a1d78-119">Вы можете использовать теги для идентификации шлюза из других ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d78-119">You can use tags to identify a Gateway from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d78-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d78-120">-DefaultProfile</span></span>
<span data-ttu-id="a1d78-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d78-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1d78-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d78-122">CommonParameters</span></span>
<span data-ttu-id="a1d78-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1d78-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d78-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1d78-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d78-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1d78-125">INPUTS</span></span>

## <span data-ttu-id="a1d78-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1d78-126">OUTPUTS</span></span>

### <span data-ttu-id="a1d78-127">Microsoft. Azure. Commands. ServerManagement. Model. Gateway</span><span class="sxs-lookup"><span data-stu-id="a1d78-127">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="a1d78-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1d78-128">NOTES</span></span>

## <span data-ttu-id="a1d78-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1d78-129">RELATED LINKS</span></span>

[<span data-ttu-id="a1d78-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a1d78-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="a1d78-131">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a1d78-131">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


