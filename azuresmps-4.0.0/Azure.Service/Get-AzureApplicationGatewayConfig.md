---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075665"
---
# <span data-ttu-id="3caf4-101">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="3caf4-101">Get-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="3caf4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3caf4-102">SYNOPSIS</span></span>
<span data-ttu-id="3caf4-103">Возвращает контекст конфигурации шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3caf4-103">Gets an Application Gateway configuration context.</span></span>

## <span data-ttu-id="3caf4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3caf4-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3caf4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3caf4-105">DESCRIPTION</span></span>
<span data-ttu-id="3caf4-106">Командлет **Get-AzureApplicationGatewayConfig** получает контекст конфигурации шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="3caf4-106">The **Get-AzureApplicationGatewayConfig** cmdlet gets an Azure Application Gateway configuration context.</span></span>
<span data-ttu-id="3caf4-107">Контекст включает в себя как объект конфигурации, так и конфигурацию XML.</span><span class="sxs-lookup"><span data-stu-id="3caf4-107">A context includes both a configuration object and XML configuration.</span></span>
<span data-ttu-id="3caf4-108">Вы можете сохранить конфигурацию XML в файле.</span><span class="sxs-lookup"><span data-stu-id="3caf4-108">You can save the XML configuration to a file.</span></span>

## <span data-ttu-id="3caf4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3caf4-109">EXAMPLES</span></span>

### <span data-ttu-id="3caf4-110">Пример 1: получение конфигурации шлюза приложений и сохранение ее в файле</span><span class="sxs-lookup"><span data-stu-id="3caf4-110">Example 1: Get an Application Gateway configuration and save it to a file</span></span>
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

<span data-ttu-id="3caf4-111">Эта команда получает конфигурацию для шлюза приложения с именем ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="3caf4-111">This command gets the configuration for an Application Gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="3caf4-112">Команда сохраняет его в файле в указанном пути.</span><span class="sxs-lookup"><span data-stu-id="3caf4-112">The command saves it in the file in the specified path.</span></span>

## <span data-ttu-id="3caf4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3caf4-113">PARAMETERS</span></span>

### <span data-ttu-id="3caf4-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="3caf4-114">-ExportToFile</span></span>
<span data-ttu-id="3caf4-115">Задает путь к файлу, на который этот командлет сохраняет конфигурацию в формате XML.</span><span class="sxs-lookup"><span data-stu-id="3caf4-115">Specifies a file path to which this cmdlet saves the configuration in XML format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caf4-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3caf4-116">-Name</span></span>
<span data-ttu-id="3caf4-117">Указывает имя шлюза приложений, для которого этот командлет получает сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3caf4-117">Specifies the name of the Application Gateway for which this cmdlet gets configuration information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3caf4-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="3caf4-118">-Profile</span></span>
<span data-ttu-id="3caf4-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3caf4-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3caf4-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3caf4-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caf4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3caf4-121">CommonParameters</span></span>
<span data-ttu-id="3caf4-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3caf4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3caf4-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3caf4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3caf4-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3caf4-124">INPUTS</span></span>

### <span data-ttu-id="3caf4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3caf4-125">System.String</span></span>

## <span data-ttu-id="3caf4-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3caf4-126">OUTPUTS</span></span>

### <span data-ttu-id="3caf4-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext</span><span class="sxs-lookup"><span data-stu-id="3caf4-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfigContext</span></span>

## <span data-ttu-id="3caf4-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="3caf4-128">NOTES</span></span>

## <span data-ttu-id="3caf4-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3caf4-129">RELATED LINKS</span></span>

[<span data-ttu-id="3caf4-130">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="3caf4-130">Set-AzureApplicationGatewayConfig</span></span>](./Set-AzureApplicationGatewayConfig.md)


