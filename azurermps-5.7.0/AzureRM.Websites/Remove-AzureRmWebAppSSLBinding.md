---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 46ea58d66efbde588b1f7677477d3b7521b1d02c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561295"
---
# <span data-ttu-id="bab90-101">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="bab90-101">Remove-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="bab90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bab90-102">SYNOPSIS</span></span>
<span data-ttu-id="bab90-103">Удаление привязки SSL из отправленного сертификата.</span><span class="sxs-lookup"><span data-stu-id="bab90-103">Removes an SSL binding from an uploaded certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bab90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bab90-104">SYNTAX</span></span>

### <span data-ttu-id="bab90-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="bab90-105">S1</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bab90-106">S2</span><span class="sxs-lookup"><span data-stu-id="bab90-106">S2</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bab90-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bab90-107">DESCRIPTION</span></span>
<span data-ttu-id="bab90-108">Командлет **Remove-AzureRmWebAppSSLBinding** удаляет привязку SSL (Secure Sockets Layer) из веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="bab90-108">The **Remove-AzureRmWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="bab90-109">Привязки SSL используются для связывания веб-приложения с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="bab90-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="bab90-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bab90-110">EXAMPLES</span></span>

### <span data-ttu-id="bab90-111">Пример 1: удаление привязки SSL для веб-приложения</span><span class="sxs-lookup"><span data-stu-id="bab90-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="bab90-112">Эта команда удаляет привязку SSL для веб-приложения ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="bab90-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="bab90-113">Так как параметр *DeleteCertificate* не включен, сертификат будет удален, если он больше не имеет каких-либо SSL-привязок.</span><span class="sxs-lookup"><span data-stu-id="bab90-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="bab90-114">Пример 2: удаление привязки SSL без удаления сертификата</span><span class="sxs-lookup"><span data-stu-id="bab90-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="bab90-115">Как и в примере 1, эта команда также удаляет привязку SSL для веб-приложения ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="bab90-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="bab90-116">Тем не менее, в этом случае параметр *DeleteCertificate* включается, и значение параметра задается равным $false.</span><span class="sxs-lookup"><span data-stu-id="bab90-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="bab90-117">Это означает, что сертификат не будет удален независимо от того, есть ли у него привязки SSL или нет.</span><span class="sxs-lookup"><span data-stu-id="bab90-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="bab90-118">Пример 3: использование ссылки на объект для удаления привязки SSL</span><span class="sxs-lookup"><span data-stu-id="bab90-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="bab90-119">В этом примере для удаления привязки SSL для веб-приложения используется ссылка на объект веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="bab90-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>

<span data-ttu-id="bab90-120">Первая команда использует командлет Get-AzureRmWebApp для создания ссылки на объект веб-приложения с именем ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="bab90-120">The first command uses the Get-AzureRmWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="bab90-121">Ссылка на объект хранится в переменной с именем $WebApp.</span><span class="sxs-lookup"><span data-stu-id="bab90-121">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="bab90-122">Вторая команда использует ссылку на объект и командлет **Remove-AzureRmWebAppSSLBinding** для удаления привязки SSL.</span><span class="sxs-lookup"><span data-stu-id="bab90-122">The second command uses the object reference and the **Remove-AzureRmWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="bab90-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bab90-123">PARAMETERS</span></span>

### <span data-ttu-id="bab90-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab90-124">-DefaultProfile</span></span>
<span data-ttu-id="bab90-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bab90-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bab90-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="bab90-126">-DeleteCertificate</span></span>
<span data-ttu-id="bab90-127">Указывает действие, которое будет выполнено, если удаляемая привязка SSL является единственной привязкой, используемой сертификатом.</span><span class="sxs-lookup"><span data-stu-id="bab90-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="bab90-128">Если для *DeleteCertificate* задано значение $false, сертификат не будет удален при удалении привязки.</span><span class="sxs-lookup"><span data-stu-id="bab90-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="bab90-129">Если *DeleteCertificate* имеет значение $true или не включено в команду, сертификат будет удален вместе с привязкой SSL.</span><span class="sxs-lookup"><span data-stu-id="bab90-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>

<span data-ttu-id="bab90-130">Сертификат будет удален только в том случае, если удаляемая привязка SSL является единственной привязкой, используемой сертификатом.</span><span class="sxs-lookup"><span data-stu-id="bab90-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="bab90-131">Если у сертификата есть более одной привязки, сертификат не будет удален независимо от значения параметра *DeleteCertificate* .</span><span class="sxs-lookup"><span data-stu-id="bab90-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab90-132">-Force</span><span class="sxs-lookup"><span data-stu-id="bab90-132">-Force</span></span>
<span data-ttu-id="bab90-133">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bab90-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab90-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bab90-134">-Name</span></span>
<span data-ttu-id="bab90-135">Указывает имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="bab90-135">Specifies the name of the Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab90-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bab90-136">-ResourceGroupName</span></span>
<span data-ttu-id="bab90-137">Указывает имя группы ресурсов, которой назначен сертификат.</span><span class="sxs-lookup"><span data-stu-id="bab90-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="bab90-138">В одной команде нельзя использовать параметры *ResourceGroupName* и *webapp* .</span><span class="sxs-lookup"><span data-stu-id="bab90-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="bab90-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="bab90-139">-Slot</span></span>
<span data-ttu-id="bab90-140">Указывает слот развертывания веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="bab90-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="bab90-141">Чтобы получить слот развертывания, используйте командлет Get-AzureRMWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="bab90-141">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="bab90-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bab90-142">-WebApp</span></span>
<span data-ttu-id="bab90-143">Указывает веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="bab90-143">Specifies a Web App.</span></span>
<span data-ttu-id="bab90-144">Чтобы получить веб-приложение, используйте командлет Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="bab90-144">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="bab90-145">Параметр *webapp* нельзя использовать в той же команде, что и параметр *ResourceGroupName* , и (или) *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="bab90-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="bab90-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="bab90-146">-WebAppName</span></span>
<span data-ttu-id="bab90-147">Указывает имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="bab90-147">Specifies the name of the Web App.</span></span>

<span data-ttu-id="bab90-148">В одной команде нельзя использовать параметры *WebAppName* и *webapp* .</span><span class="sxs-lookup"><span data-stu-id="bab90-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="bab90-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bab90-149">-Confirm</span></span>
<span data-ttu-id="bab90-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bab90-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab90-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bab90-151">-WhatIf</span></span>
<span data-ttu-id="bab90-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bab90-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bab90-153">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bab90-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bab90-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bab90-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab90-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab90-155">CommonParameters</span></span>
<span data-ttu-id="bab90-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bab90-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab90-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bab90-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab90-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bab90-158">INPUTS</span></span>

### <span data-ttu-id="bab90-159">Семейств</span><span class="sxs-lookup"><span data-stu-id="bab90-159">Site</span></span>
<span data-ttu-id="bab90-160">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bab90-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bab90-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bab90-161">OUTPUTS</span></span>

## <span data-ttu-id="bab90-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="bab90-162">NOTES</span></span>

## <span data-ttu-id="bab90-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bab90-163">RELATED LINKS</span></span>

[<span data-ttu-id="bab90-164">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="bab90-164">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="bab90-165">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="bab90-165">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="bab90-166">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bab90-166">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="bab90-167">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bab90-167">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


