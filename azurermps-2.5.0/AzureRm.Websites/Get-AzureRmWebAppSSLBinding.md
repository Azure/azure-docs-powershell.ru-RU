---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 103c5e75b433fcb585113e8ef6bc89aab1f82d7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913530"
---
# <span data-ttu-id="f6904-101">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f6904-101">Get-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="f6904-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6904-102">SYNOPSIS</span></span>
<span data-ttu-id="f6904-103">Получение привязки SSL сертификата веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="f6904-103">Gets an Azure Web App certificate SSL binding.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6904-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6904-104">SYNTAX</span></span>

### <span data-ttu-id="f6904-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="f6904-105">S1</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6904-106">S2</span><span class="sxs-lookup"><span data-stu-id="f6904-106">S2</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6904-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6904-107">DESCRIPTION</span></span>
<span data-ttu-id="f6904-108">Командлет **Get-AzureRmWebAppSSLBinding** получает для веб-приложения Azure привязку SSL (Secure socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="f6904-108">The **Get-AzureRmWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="f6904-109">Привязки SSL используются для связывания веб-приложения с отправленным сертификатом.</span><span class="sxs-lookup"><span data-stu-id="f6904-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="f6904-110">Веб-приложения можно привязать к нескольким сертификатам.</span><span class="sxs-lookup"><span data-stu-id="f6904-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="f6904-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6904-111">EXAMPLES</span></span>

### <span data-ttu-id="f6904-112">Пример 1: получение привязок SSL для веб-приложения</span><span class="sxs-lookup"><span data-stu-id="f6904-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="f6904-113">Эта команда извлекает привязки SSL для веб-приложения ContosoWebApp, связанного с группой ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f6904-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="f6904-114">Пример 2: использование ссылки на объект для получения привязок SSL для веб-приложения</span><span class="sxs-lookup"><span data-stu-id="f6904-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="f6904-115">Команды в этом примере также получают привязки SSL для веб-приложения ContosoWebApp; Однако в этом случае вместо имени веб-приложения и имени связанной группы ресурсов используется ссылка на объект.</span><span class="sxs-lookup"><span data-stu-id="f6904-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="f6904-116">Эта ссылка на объект создана первой командой в примере, которая использует **Get-AzureRmWebApp** для создания ссылки на объект веб-приложения с именем ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="f6904-116">This object reference is created by the first command in the example, which uses **Get-AzureRmWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="f6904-117">Ссылка на объект хранится в переменной с именем $WebApp.</span><span class="sxs-lookup"><span data-stu-id="f6904-117">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="f6904-118">Эта переменная и командлет **Get-AzureRmWebAppSSLBinding** используются второй командой для получения привязок SSL.</span><span class="sxs-lookup"><span data-stu-id="f6904-118">This variable, and the **Get-AzureRmWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="f6904-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6904-119">PARAMETERS</span></span>

### <span data-ttu-id="f6904-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6904-120">-DefaultProfile</span></span>
<span data-ttu-id="f6904-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6904-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6904-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6904-122">-Name</span></span>
<span data-ttu-id="f6904-123">Указывает имя привязки SSL.</span><span class="sxs-lookup"><span data-stu-id="f6904-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6904-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6904-124">-ResourceGroupName</span></span>
<span data-ttu-id="f6904-125">Указывает имя группы ресурсов, которой назначен сертификат.</span><span class="sxs-lookup"><span data-stu-id="f6904-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="f6904-126">В одной команде нельзя использовать параметры *ResourceGroupName* и *webapp* .</span><span class="sxs-lookup"><span data-stu-id="f6904-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6904-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="f6904-127">-Slot</span></span>
<span data-ttu-id="f6904-128">Указывает слот развертывания веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f6904-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="f6904-129">Чтобы получить слот развертывания, используйте командлет Get-AzureRMWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="f6904-129">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6904-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f6904-130">-WebApp</span></span>
<span data-ttu-id="f6904-131">Указывает веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="f6904-131">Specifies a Web App.</span></span>
<span data-ttu-id="f6904-132">Чтобы получить веб-приложение, используйте командлет Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="f6904-132">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6904-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="f6904-133">-WebAppName</span></span>
<span data-ttu-id="f6904-134">Указывает имя веб-приложения, из которого этот командлет получает привязки SSL.</span><span class="sxs-lookup"><span data-stu-id="f6904-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>

<span data-ttu-id="f6904-135">В одной команде нельзя использовать параметры *WebAppName* и *webapp* .</span><span class="sxs-lookup"><span data-stu-id="f6904-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6904-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6904-136">CommonParameters</span></span>
<span data-ttu-id="f6904-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6904-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6904-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6904-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6904-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6904-139">INPUTS</span></span>

### <span data-ttu-id="f6904-140">Семейств</span><span class="sxs-lookup"><span data-stu-id="f6904-140">Site</span></span>
<span data-ttu-id="f6904-141">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f6904-141">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f6904-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6904-142">OUTPUTS</span></span>

## <span data-ttu-id="f6904-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6904-143">NOTES</span></span>

## <span data-ttu-id="f6904-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6904-144">RELATED LINKS</span></span>

[<span data-ttu-id="f6904-145">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f6904-145">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="f6904-146">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f6904-146">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="f6904-147">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f6904-147">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


