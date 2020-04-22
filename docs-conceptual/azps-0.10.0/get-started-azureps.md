---
title: Начало работы с Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/17/2020
ms.openlocfilehash: 718f0dc0f1ef9b0c2aa3d0630ca099fa5cec7ec0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "81445719"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="309ba-102">Начало работы с Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="309ba-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="309ba-103">Среда Azure PowerShell оптимизирована для администрирования ресурсов Azure и управления ими из командной строки.</span><span class="sxs-lookup"><span data-stu-id="309ba-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="309ba-104">С помощью Azure PowerShell можно создавать автоматизированные средства на основе модели Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="309ba-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="309ba-105">Попробуйте использовать его в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="309ba-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="309ba-106">В этой статье содержатся инструкции по началу работы с Azure PowerShell и объясняются основные принципы работы этой среды.</span><span class="sxs-lookup"><span data-stu-id="309ba-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="309ba-107">Установка или запуск в Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="309ba-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="309ba-108">Проще всего начать работу с Azure PowerShell в среде Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="309ba-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="309ba-109">Чтобы начать работу с Cloud Shell, см. [Краткое руководство по использованию PowerShell в Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="309ba-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="309ba-110">Cloud Shell запускает PowerShell 6 в контейнере Linux, поэтому специальные функции Windows будут недоступны.</span><span class="sxs-lookup"><span data-stu-id="309ba-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="309ba-111">Когда все будет готово к установке Azure PowerShell на локальный компьютер, следуйте инструкциям, приведенным в статье [Install the Azure PowerShell module](install-az-ps.md) (Установка модуля Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="309ba-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="309ba-112">Вход в Azure</span><span class="sxs-lookup"><span data-stu-id="309ba-112">Sign in to Azure</span></span>

<span data-ttu-id="309ba-113">Войдите в учетную запись в интерактивном режиме с помощью командлета `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="309ba-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="309ba-114">При использовании Cloud Shell этот шаг можно пропустить: Сеанс Azure Cloud Shell уже прошел аутентификацию для среды, подписки и клиента, который запустил сеанс Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="309ba-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="309ba-115">Если вы находитесь за пределами США, используйте для входа параметр `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="309ba-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="309ba-116">Имя среды для вашего региона можно получить с помощью командлета [Get AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).</span><span class="sxs-lookup"><span data-stu-id="309ba-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="309ba-117">Например, для входа в учетную запись Azure China 21Vianet выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="309ba-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="309ba-118">В средах PowerShell 5.1 используется диалоговое окно для входа, в котором можно указать имя пользователя и пароль для учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="309ba-118">In PowerShell 5.1 environments, you'll get a sign-in dialog to provide a username and password for your Azure account.</span></span> <span data-ttu-id="309ba-119">В любой другой версии PowerShell вы получите маркер для использования в [https://microsoft.com/devicelogin ].</span><span class="sxs-lookup"><span data-stu-id="309ba-119">On every other version of PowerShell, you'll get a token to use on [https://microsoft.com/devicelogin].</span></span>
<span data-ttu-id="309ba-120">Откройте эту страницу в браузере и введите токен, чтобы войти с данными учетной записи Azure и авторизовать Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="309ba-120">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span>

<span data-ttu-id="309ba-121">После входа вам отобразится информация о ваших активных подписках Azure.</span><span class="sxs-lookup"><span data-stu-id="309ba-121">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="309ba-122">Если в вашей учетной записи есть несколько подписок Azure и вы хотите выбрать другую, получите список доступных подписок с помощью командлета [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) и выполните командлет [Set-AzContext](/powershell/module/az.accounts/set-azcontext) с указанием идентификатора своей подписки.</span><span class="sxs-lookup"><span data-stu-id="309ba-122">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="309ba-123">Дополнительные сведения об управлении подписками Azure в Azure PowerShell см. в статье [Use multiple Azure subscriptions](manage-subscriptions-azureps.md) (Использование нескольких подписок Azure).</span><span class="sxs-lookup"><span data-stu-id="309ba-123">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="309ba-124">После входа в учетную запись Azure вы можете использовать командлеты Azure PowerShell для доступа и управления ресурсами в подписке.</span><span class="sxs-lookup"><span data-stu-id="309ba-124">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="309ba-125">Дополнительные сведения о процессе входа и методах проверки подлинности см. в статье [Вход с помощью Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="309ba-125">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="309ba-126">Поиск команд</span><span class="sxs-lookup"><span data-stu-id="309ba-126">Find commands</span></span>

<span data-ttu-id="309ba-127">В Azure PowerShell названия командлетов выбираются в соответствии со стандартным соглашением об именовании для PowerShell — `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="309ba-127">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="309ba-128">Глагол (часть verb) отвечает за действие (к ним относятся `New`, `Get`, `Set`, `Remove`), а существительное (часть noun) — за тип ресурса (к ним относятся `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="309ba-128">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="309ba-129">В Azure PowerShell существительное всегда начинается с префикса `Az`.</span><span class="sxs-lookup"><span data-stu-id="309ba-129">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="309ba-130">Полный список стандартных глаголов см. в разделе [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands) (Утвержденные глаголы для команд PowerShell).</span><span class="sxs-lookup"><span data-stu-id="309ba-130">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="309ba-131">Если вы знаете существительные и глаголы, с помощью модулей Azure PowerShell можно найти команды, выполнив командлет [Get-Command](/powershell/module/microsoft.powershell.core/get-command).</span><span class="sxs-lookup"><span data-stu-id="309ba-131">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="309ba-132">Например, чтобы найти все связанные с виртуальной машиной команды, в которых используется глагол `Get` выполните следующий код:</span><span class="sxs-lookup"><span data-stu-id="309ba-132">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="309ba-133">Чтобы облегчить поиск часто используемых команд, в таблице ниже приведены типы ресурсов, указан соответствующий модуль Azure PowerShell и префикс для использования с командой `Get-Command`:</span><span class="sxs-lookup"><span data-stu-id="309ba-133">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="309ba-134">Тип ресурса</span><span class="sxs-lookup"><span data-stu-id="309ba-134">Resource type</span></span> | <span data-ttu-id="309ba-135">модуль Azure PowerShell;</span><span class="sxs-lookup"><span data-stu-id="309ba-135">Azure PowerShell module</span></span> | <span data-ttu-id="309ba-136">Префикс в существительном</span><span class="sxs-lookup"><span data-stu-id="309ba-136">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="309ba-137">Группа ресурсов</span><span class="sxs-lookup"><span data-stu-id="309ba-137">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="309ba-138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="309ba-138">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="309ba-139">Виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="309ba-139">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="309ba-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="309ba-140">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="309ba-141">Учетные записи хранения</span><span class="sxs-lookup"><span data-stu-id="309ba-141">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="309ba-142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="309ba-142">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="309ba-143">хранилище ключей;</span><span class="sxs-lookup"><span data-stu-id="309ba-143">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="309ba-144">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="309ba-144">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="309ba-145">Веб-приложения</span><span class="sxs-lookup"><span data-stu-id="309ba-145">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="309ba-146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="309ba-146">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="309ba-147">Базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="309ba-147">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="309ba-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="309ba-148">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="309ba-149">Полный список модулей для Azure PowerShell см. на [этой странице](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) сайта GitHub.</span><span class="sxs-lookup"><span data-stu-id="309ba-149">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="309ba-150">Дополнительные сведения об основах работы с Azure PowerShell приведены в кратких руководствах и других материалах</span><span class="sxs-lookup"><span data-stu-id="309ba-150">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="309ba-151">Чтобы начать работу с Azure PowerShell, ознакомьтесь с подробным руководством по настройке виртуальных машин и отправке запросов на получение данных.</span><span class="sxs-lookup"><span data-stu-id="309ba-151">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="309ba-152">Создание виртуальных машин с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="309ba-152">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="309ba-153">Кроме того, можно воспользоваться краткими руководствами по Azure PowerShell для других популярных служб Azure:</span><span class="sxs-lookup"><span data-stu-id="309ba-153">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="309ba-154">создать учетную запись хранения;</span><span class="sxs-lookup"><span data-stu-id="309ba-154">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="309ba-155">Передача объектов в хранилище BLOB-объектов Azure и из него</span><span class="sxs-lookup"><span data-stu-id="309ba-155">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="309ba-156">Создание и извлечение секретов из Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="309ba-156">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="309ba-157">Создание базы данных Azure SQL и брандмауэра</span><span class="sxs-lookup"><span data-stu-id="309ba-157">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="309ba-158">Запуск контейнеров в службе "Экземпляры контейнеров Azure"</span><span class="sxs-lookup"><span data-stu-id="309ba-158">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="309ba-159">Создание масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="309ba-159">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="309ba-160">Создание подсистемы балансировки нагрузки уровня "Стандартный"</span><span class="sxs-lookup"><span data-stu-id="309ba-160">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="309ba-161">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="309ba-161">Next steps</span></span>

* [<span data-ttu-id="309ba-162">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="309ba-162">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="309ba-163">Управление подписками Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="309ba-163">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="309ba-164">Создание субъектов-служб Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="309ba-164">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="309ba-165">Помощь от сообщества:</span><span class="sxs-lookup"><span data-stu-id="309ba-165">Get help from the community:</span></span>
  * [<span data-ttu-id="309ba-166">Форум Azure на MSDN</span><span class="sxs-lookup"><span data-stu-id="309ba-166">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="309ba-167">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="309ba-167">Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
