---
title: Все отличия между AzureRM и Az версии 1.0.0 для Azure PowerShell
description: Это руководство по миграции содержит список критических изменений, внесенных в выпуск Az версии 1 в Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 3ab12307f786c12422338835926802793a33713e
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715836"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="cd5f6-103">Критические изменения для Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cd5f6-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="cd5f6-104">В этом документе содержатся подробные сведения об отличиях между AzureRM 6.x и новым модулем Az версии 1.x и более поздних.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="cd5f6-105">Пункты в оглавлении помогут вам разобраться со всеми этапами переноса, включая изменения модуля, которые могут повлиять на скрипты.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="cd5f6-106">Общие советы по началу перехода с Az на AzureRM см. в [этой статье](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="cd5f6-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd5f6-107">Кроме того, после выхода версии Az 1.0.0 также были внесены критические изменения, которые представлены в Az 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-107">There have been breaking changes between Az 1.0.0 and Az 2.0.0 as well.</span></span> <span data-ttu-id="cd5f6-108">Выполнив действия по переходу с AzureRM на Az, представленные в этом руководстве, перейдите к статье [о критических изменениях в Az 2.0.0](migrate-az-2.0.0.md), чтобы узнать, необходимо ли вам внести дополнительные изменения.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-108">After following this guide for updating from AzureRM to Az, see the [Az 2.0.0 breaking changes](migrate-az-2.0.0.md) to find out if you need to make additional changes.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="cd5f6-109">Оглавление</span><span class="sxs-lookup"><span data-stu-id="cd5f6-109">Table of Contents</span></span>

- [<span data-ttu-id="cd5f6-110">Общие критически важные изменения</span><span class="sxs-lookup"><span data-stu-id="cd5f6-110">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="cd5f6-111">Изменения префикса существительного командлета</span><span class="sxs-lookup"><span data-stu-id="cd5f6-111">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="cd5f6-112">Изменение имени модуля</span><span class="sxs-lookup"><span data-stu-id="cd5f6-112">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="cd5f6-113">Удаленные модули</span><span class="sxs-lookup"><span data-stu-id="cd5f6-113">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="cd5f6-114">Windows PowerShell 5.1 и .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="cd5f6-114">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="cd5f6-115">Временное удаление входа пользователя с помощью PSCredential</span><span class="sxs-lookup"><span data-stu-id="cd5f6-115">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="cd5f6-116">Вход с кодом устройства по умолчанию вместо запроса веб-браузера</span><span class="sxs-lookup"><span data-stu-id="cd5f6-116">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="cd5f6-117">Критические изменения модуля</span><span class="sxs-lookup"><span data-stu-id="cd5f6-117">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="cd5f6-118">Az.ApiManagement (ранее AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-118">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="cd5f6-119">Az.Billing (ранее AzureRM.Billing, AzureRM.Consitation и AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-119">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="cd5f6-120">Az.CognitiveServices (ранее AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-120">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="cd5f6-121">Az.Compute (ранее AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-121">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="cd5f6-122">Az.DataFactory (ранее AzureRM.DataFactories и AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-122">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="cd5f6-123">Az.DataLakeAnalytics (ранее AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-123">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="cd5f6-124">Az.DataLakeStore (ранее AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-124">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="cd5f6-125">Az.KeyVault (ранее AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-125">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="cd5f6-126">Az.Media (ранее AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-126">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="cd5f6-127">Az.Monitor (ранее AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-127">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="cd5f6-128">Az.Network (ранее AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-128">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="cd5f6-129">Az.OperationalInsights (ранее AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-129">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="cd5f6-130">Az.RecoveryServices (ранее AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup и AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-130">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="cd5f6-131">Az.Resources (ранее AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-131">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="cd5f6-132">Az.ServiceFabric (ранее AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-132">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="cd5f6-133">Az.Sql (ранее AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-133">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="cd5f6-134">Az.Storage (ранее Azure.Storage и AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-134">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="cd5f6-135">Az.Websites (ранее AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-135">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="cd5f6-136">Общие критически важные изменения</span><span class="sxs-lookup"><span data-stu-id="cd5f6-136">General breaking changes</span></span>

<span data-ttu-id="cd5f6-137">В этом разделе описаны общие критические изменения, которые являются частью этой переработанной версии модуля Az.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-137">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="cd5f6-138">Изменения префикса существительного командлета</span><span class="sxs-lookup"><span data-stu-id="cd5f6-138">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="cd5f6-139">В модуле AzureRM в существительных командлетов используется префикс `AzureRM` или `Azure`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-139">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="cd5f6-140">Az упрощает и нормализует имена командлетов, так что все командлеты используют "Az" в качестве префикса существительного командлета.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-140">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="cd5f6-141">Например:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-141">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="cd5f6-142">изменено на:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-142">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="cd5f6-143">Чтобы упростить переход на эти новые имена командлетов, Az представляет два новых командлета: [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) и [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="cd5f6-143">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="cd5f6-144">`Enable-AzureRmAlias` создает псевдонимы для старых имен командлетов в AzureRM, которые сопоставляются с новыми именами командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-144">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="cd5f6-145">Используя аргумент `-Scope` с командлетом `Enable-AzureRmAlias`, вы можете выбрать, в контексте чего будут включены псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-145">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="cd5f6-146">Следующий сценарий в AzureRM является примером.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-146">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="cd5f6-147">Его можно выполнить с минимальными изменениями с помощью `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-147">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="cd5f6-148">При выполнении `Enable-AzureRmAlias -Scope CurrentUser` псевдонимы будут включены для всех открытых сеансов PowerShell, так что после выполнения этого командлета такой сценарий не нужно будет изменять.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-148">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="cd5f6-149">Дополнительные сведения об использовании командлетов псевдонимов см. в [справочнике по командлету Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="cd5f6-149">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="cd5f6-150">Когда вы будете готовы отключить псевдонимы, запустите командлет `Disable-AzureRmAlias`, который удаляет созданные псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-150">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="cd5f6-151">Дополнительные сведения см. в [справочнике по командлету Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="cd5f6-151">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd5f6-152">Убедитесь, что отключили псевдонимы для _всех_ областей, в которых они были включены.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-152">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="cd5f6-153">Изменение имени модуля</span><span class="sxs-lookup"><span data-stu-id="cd5f6-153">Module Name Changes</span></span>

<span data-ttu-id="cd5f6-154">Имена модулей изменены с `AzureRM.*` на `Az.*`, за исключением следующих модулей.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-154">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="cd5f6-155">Модуль AzureRM</span><span class="sxs-lookup"><span data-stu-id="cd5f6-155">AzureRM module</span></span> | <span data-ttu-id="cd5f6-156">Модуль Az</span><span class="sxs-lookup"><span data-stu-id="cd5f6-156">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="cd5f6-157">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-157">Azure.Storage</span></span> | <span data-ttu-id="cd5f6-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd5f6-158">Az.Storage</span></span> |
| <span data-ttu-id="cd5f6-159">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd5f6-159">Azure.AnalysisServices</span></span> | <span data-ttu-id="cd5f6-160">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd5f6-160">Az.AnalysisServices</span></span> |
| <span data-ttu-id="cd5f6-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="cd5f6-161">AzureRM.Profile</span></span> | <span data-ttu-id="cd5f6-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd5f6-162">Az.Accounts</span></span> |
| <span data-ttu-id="cd5f6-163">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-163">AzureRM.Insights</span></span> | <span data-ttu-id="cd5f6-164">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd5f6-164">Az.Monitor</span></span> |
| <span data-ttu-id="cd5f6-165">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="cd5f6-165">AzureRM.DataFactories</span></span> | <span data-ttu-id="cd5f6-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd5f6-166">Az.DataFactory</span></span> |
| <span data-ttu-id="cd5f6-167">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cd5f6-167">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="cd5f6-168">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd5f6-168">Az.DataFactory</span></span> |
| <span data-ttu-id="cd5f6-169">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cd5f6-169">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="cd5f6-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd5f6-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="cd5f6-171">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="cd5f6-171">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="cd5f6-172">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd5f6-172">Az.RecoveryServices</span></span> |
| <span data-ttu-id="cd5f6-173">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="cd5f6-173">AzureRM.Tags</span></span> | <span data-ttu-id="cd5f6-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd5f6-174">Az.Resources</span></span> |
| <span data-ttu-id="cd5f6-175">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="cd5f6-175">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="cd5f6-176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cd5f6-176">Az.MachineLearning</span></span> |
| <span data-ttu-id="cd5f6-177">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="cd5f6-177">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="cd5f6-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cd5f6-178">Az.Billing</span></span> |
| <span data-ttu-id="cd5f6-179">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-179">AzureRM.Consumption</span></span> | <span data-ttu-id="cd5f6-180">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cd5f6-180">Az.Billing</span></span> |

<span data-ttu-id="cd5f6-181">Изменения в именах модулей означают, что любой сценарий, который использует `#Requires` или `Import-Module` для загрузки определенных модулей, необходимо будет изменить, чтобы вместо него использовать новый модуль.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-181">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="cd5f6-182">Для модулей, в которых суффикс командлета не был изменен, это означает, что хотя имя модуля изменилось, суффикс, указывающий пространство операции, _не изменился_.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-182">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="cd5f6-183">Перенос инструкций #Requires и Import-Module</span><span class="sxs-lookup"><span data-stu-id="cd5f6-183">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="cd5f6-184">Скрипты, объявляющие зависимости от модулей AzureRM с помощью `#Requires` или `Import-Module`, должны быть обновлены для использования новых имен модулей.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-184">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="cd5f6-185">Например:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-185">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="cd5f6-186">следует изменить на</span><span class="sxs-lookup"><span data-stu-id="cd5f6-186">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="cd5f6-187">Для `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-187">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="cd5f6-188">следует изменить на</span><span class="sxs-lookup"><span data-stu-id="cd5f6-188">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="cd5f6-189">Миграция вызовов командлета Fully-Qualified</span><span class="sxs-lookup"><span data-stu-id="cd5f6-189">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="cd5f6-190">Скрипты, использующие вызовы командлетов с указанием модуля, например:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-190">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="cd5f6-191">Следует изменить, чтобы использовать новые имена модулей и командлетов:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-191">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="cd5f6-192">Перенос зависимостей манифеста модуля</span><span class="sxs-lookup"><span data-stu-id="cd5f6-192">Migrating module manifest dependencies</span></span>

<span data-ttu-id="cd5f6-193">Модули, которые выражают зависимости от модулей AzureRM через файл манифеста модуля (PSD1), должны обновить имена модулей в разделе `RequiredModules`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-193">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="cd5f6-194">Необходимо изменить на:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-194">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="cd5f6-195">Удаленные модули</span><span class="sxs-lookup"><span data-stu-id="cd5f6-195">Removed modules</span></span>

<span data-ttu-id="cd5f6-196">Следующие модули удалены:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-196">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="cd5f6-197">Средства для работы с этими службами больше не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-197">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="cd5f6-198">Клиентам рекомендуется обратиться к альтернативным службам, как только появится возможность.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-198">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="cd5f6-199">Windows PowerShell 5.1 и .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="cd5f6-199">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="cd5f6-200">Для использования Az с PowerShell 5.1 для Windows требуется установить .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-200">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="cd5f6-201">Для использования PowerShell Core 6.x или более поздней версии .NET Framework не требуется.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-201">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="cd5f6-202">Временное удаление входа пользователя с помощью PSCredential</span><span class="sxs-lookup"><span data-stu-id="cd5f6-202">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="cd5f6-203">Из-за изменений в процессе проверки подлинности для .NET Standard мы временно удаляем вход пользователя через PSCredential.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-203">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="cd5f6-204">Эта возможность будет доступна в выпуске от 15 января 2019 г. для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-204">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="cd5f6-205">Это подробно описано в [этом сообщении на сайте GitHub](https://github.com/Azure/azure-powershell/issues/7430).</span><span class="sxs-lookup"><span data-stu-id="cd5f6-205">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="cd5f6-206">Вход с кодом устройства по умолчанию вместо запроса веб-браузера</span><span class="sxs-lookup"><span data-stu-id="cd5f6-206">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="cd5f6-207">Из-за изменений в процессе проверки подлинности для .NET Standard мы используем вход устройства в качестве потока входа по умолчанию во время интерактивного входа.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-207">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="cd5f6-208">Вход через веб-браузер будет повторно представлен для Windows PowerShell 5.1 в качестве версии по умолчанию в выпуске от 15 января 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-208">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="cd5f6-209">В это время пользователи смогут выбрать вход устройства с помощью параметра Switch.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-209">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="cd5f6-210">Критические изменения модуля</span><span class="sxs-lookup"><span data-stu-id="cd5f6-210">Module breaking changes</span></span>

<span data-ttu-id="cd5f6-211">В этом разделе описаны конкретные критические изменения для отдельных модулей и командлетов.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-211">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="cd5f6-212">Az.ApiManagement (ранее AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-212">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="cd5f6-213">Удалены приведенные ниже командлеты.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-213">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="cd5f6-214">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd5f6-214">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="cd5f6-215">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="cd5f6-215">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="cd5f6-216">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="cd5f6-216">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="cd5f6-217">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="cd5f6-217">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="cd5f6-218">Используйте командлет **Set-AzApiManagement**, чтобы задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-218">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="cd5f6-219">Удалены приведенные ниже свойства.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-219">Removed the following properties:</span></span>
  - <span data-ttu-id="cd5f6-220">Удалены свойства: `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` и `ScmHostnameConfiguration` типа `PsApiManagementHostnameConfiguration` из `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-220">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="cd5f6-221">Вместо этого используйте: `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` и `ScmCustomHostnameConfiguration` типа `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-221">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="cd5f6-222">Свойство `StaticIPs` удалено из PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-222">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="cd5f6-223">Свойство было разделено на `PublicIPAddresses` и `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-223">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="cd5f6-224">Обязательное свойство `Location` удалено из командлета New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-224">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="cd5f6-225">Az.Billing (ранее AzureRM.Billing, AzureRM.Consitation и AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-225">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="cd5f6-226">Параметр `InvoiceName` удален из командлета `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-226">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="cd5f6-227">Для сценариев необходимо использовать другие параметры идентификации для счета.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-227">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="cd5f6-228">Az.CognitiveServices (ранее AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-228">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="cd5f6-229">Набор параметров `GetSkusWithAccountParamSetName` удален из командлета `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-229">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="cd5f6-230">Необходимо получить Skus по типу и расположению учетной записи, а не использовать ResourceGroupName и имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-230">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="cd5f6-231">Az.Compute (ранее AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-231">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="cd5f6-232">`IdentityIds` удалены из свойства `Identity` в объектах `PSVirtualMachine` и `PSVirtualMachineScaleSet`. Сценарии больше не должны использовать значение этого поля для принятия решений об обработке.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-232">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="cd5f6-233">Тип свойства `InstanceView` объекта `PSVirtualMachineScaleSetVM` изменен с `VirtualMachineInstanceView` на `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="cd5f6-233">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="cd5f6-234">Свойства `AutoOSUpgradePolicy` и `AutomaticOSUpgrade` удалены из свойства `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="cd5f6-234">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="cd5f6-235">Тип свойства `Sku` в объекте `PSSnapshotUpdate` изменен с `DiskSku` на `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="cd5f6-235">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="cd5f6-236">Параметр `VmScaleSetVMParameterSet` удален из командлета `Add-AzVMDataDisk`. Больше нельзя отдельно добавлять диск данных в виртуальную машину из масштабируемого набора.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-236">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="cd5f6-237">Az.DataFactory (ранее AzureRM.DataFactories и AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-237">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="cd5f6-238">Параметр `GatewayName` стал обязательным в командлете `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="cd5f6-238">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="cd5f6-239">Командлет `New-AzDataFactoryGatewayKey` удалено</span><span class="sxs-lookup"><span data-stu-id="cd5f6-239">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="cd5f6-240">Параметр `LinkedServiceName` удален из командлета `Get-AzDataFactoryV2ActivityRun`. Сценарии больше не должны использовать значение этого поля для принятия решений об обработке.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-240">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="cd5f6-241">Az.DataLakeAnalytics (ранее AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-241">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="cd5f6-242">Удалены следующие нерекомендуемые командлеты: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` и `Set-AzDataLakeAnalyticsCatalogSecret`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-242">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="cd5f6-243">Az.DataLakeStore (ранее AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-243">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="cd5f6-244">В следующих командлетах параметр `Encoding` изменен с типа `FileSystemCmdletProviderEncoding` на `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-244">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="cd5f6-245">Это изменение удаляет значения кодирования `String` и `Oem`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-245">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="cd5f6-246">Все остальные предыдущие значения кодирования остаются.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-246">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="cd5f6-247">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cd5f6-247">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="cd5f6-248">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="cd5f6-248">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="cd5f6-249">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="cd5f6-249">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="cd5f6-250">Удален нерекомендуемый псевдоним свойства `Tags` из командлетов `New-AzDataLakeStoreAccount` и `Set-AzDataLakeStoreAccount`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-250">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="cd5f6-251">Сценарии, которые используют</span><span class="sxs-lookup"><span data-stu-id="cd5f6-251">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="cd5f6-252">следует изменить на</span><span class="sxs-lookup"><span data-stu-id="cd5f6-252">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="cd5f6-253">Из объекта `PSDataLakeStoreAccountBasic` удалены нерекомендуемые свойства: `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-253">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="cd5f6-254">Любой сценарий, который использует `PSDatalakeStoreAccount`, возвращенный из `Get-AzDataLakeStoreAccount`, не должен ссылаться на эти свойства.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-254">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="cd5f6-255">Az.KeyVault (ранее AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-255">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="cd5f6-256">Свойство `PurgeDisabled` удалено из объектов `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` и `PSKeyVaultSecretAttributes`. Скрипты больше не должны ссылаться на свойство ```PurgeDisabled``` для принятия решений об обработке.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-256">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="cd5f6-257">Az.Media (ранее AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-257">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="cd5f6-258">Удалите нерекомендуемый псевдоним свойства `Tags` из командлета `New-AzMediaService`. Сценарии, которые используют</span><span class="sxs-lookup"><span data-stu-id="cd5f6-258">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="cd5f6-259">следует изменить на</span><span class="sxs-lookup"><span data-stu-id="cd5f6-259">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="cd5f6-260">Az.Monitor (ранее AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-260">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="cd5f6-261">Множественные имена `Categories` и `Timegrains` параметра удалены в пользу единичных имен параметров из командлета `Set-AzDiagnosticSetting`. Сценарии, которые используют</span><span class="sxs-lookup"><span data-stu-id="cd5f6-261">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="cd5f6-262">следует изменить на</span><span class="sxs-lookup"><span data-stu-id="cd5f6-262">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="cd5f6-263">Az.Network (ранее AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-263">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="cd5f6-264">Из командлета `Get-AzServiceEndpointPolicyDefinition` удален нерекомендуемый параметр `ResourceId`</span><span class="sxs-lookup"><span data-stu-id="cd5f6-264">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="cd5f6-265">Из объекта `PSVirtualNetwork` удалено нерекомендуемое свойство `EnableVmProtection`</span><span class="sxs-lookup"><span data-stu-id="cd5f6-265">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="cd5f6-266">Нерекомендуемый командлет `Set-AzVirtualNetworkGatewayVpnClientConfig` удален</span><span class="sxs-lookup"><span data-stu-id="cd5f6-266">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="cd5f6-267">Скрипты больше не должны принимать решения об обработке на основе значений этих полей.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-267">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="cd5f6-268">Az.OperationalInsights (ранее AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-268">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="cd5f6-269">Набор параметров по умолчанию для `Get-AzOperationalInsightsDataSource` удален и заменен на `ByWorkspaceNameByKind`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-269">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="cd5f6-270">Сценарии, в которых перечислены источники данных, использующие</span><span class="sxs-lookup"><span data-stu-id="cd5f6-270">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="cd5f6-271">следует изменить, чтобы указать вид</span><span class="sxs-lookup"><span data-stu-id="cd5f6-271">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="cd5f6-272">Az.RecoveryServices (ранее AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup и AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-272">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="cd5f6-273">Из командлета `New/Set-AzRecoveryServicesAsrPolicy` удален параметр `Encryption`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-273">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="cd5f6-274">Параметр `TargetStorageAccountName` теперь является обязательным для восстановления управляемого диска в командлете `Restore-AzRecoveryServicesBackupItem`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-274">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="cd5f6-275">В командлете `Restore-AzRecoveryServicesBackupItem` удалены параметры `StorageAccountName` и `StorageAccountResourceGroupName`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-275">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="cd5f6-276">В командлете `Get-AzRecoveryServicesBackupContainer` удален параметр `Name`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-276">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="cd5f6-277">Az.Resources (ранее AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-277">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="cd5f6-278">Из командлета `New/Set-AzPolicyAssignment` удален параметр `Sku`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-278">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="cd5f6-279">Параметр `Password` удален из командлетов `New-AzADServicePrincipal` и `New-AzADSpCredential`. Пароли генерируются автоматически. Сценарии, которые предоставили пароль:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-279">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="cd5f6-280">Следует изменить, чтобы получить пароль из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-280">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="cd5f6-281">Az.ServiceFabric (ранее AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-281">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="cd5f6-282">Следующие типы возвращаемого значения командлета были изменены.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-282">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="cd5f6-283">Свойство `ServiceTypeHealthPolicies` типа `ApplicationHealthPolicy` удалено.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-283">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="cd5f6-284">Свойство `ApplicationHealthPolicies` типа `ClusterUpgradeDeltaHealthPolicy` удалено.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-284">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="cd5f6-285">Свойство `OverrideUserUpgradePolicy` типа `ClusterUpgradePolicy` удалено.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-285">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="cd5f6-286">Эти изменения влияют на следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-286">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="cd5f6-287">Add-AzServiceFabricClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-287">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="cd5f6-288">Add-AzServiceFabricClusterCertificate;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-288">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="cd5f6-289">Add-AzServiceFabricNode;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-289">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="cd5f6-290">Add-AzServiceFabricNodeType;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-290">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="cd5f6-291">Get-AzServiceFabricCluster;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-291">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="cd5f6-292">Remove-AzServiceFabricClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-292">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="cd5f6-293">Remove-AzServiceFabricClusterCertificate;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-293">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="cd5f6-294">Remove-AzServiceFabricNode;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-294">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="cd5f6-295">Remove-AzServiceFabricNodeType;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-295">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="cd5f6-296">Remove-AzServiceFabricSetting;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-296">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="cd5f6-297">Set-AzServiceFabricSetting;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-297">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="cd5f6-298">Set-AzServiceFabricUpgradeType;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-298">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="cd5f6-299">Update-AzServiceFabricDurability;</span><span class="sxs-lookup"><span data-stu-id="cd5f6-299">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="cd5f6-300">Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-300">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="cd5f6-301">Az.Sql (ранее AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-301">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="cd5f6-302">Из командлета `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` удалены параметры `State` и `ResourceId`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-302">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="cd5f6-303">Удалены следующие нерекомендуемые командлеты: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-303">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="cd5f6-304">Из командлета `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` удален нерекомендуемый параметр `Current`</span><span class="sxs-lookup"><span data-stu-id="cd5f6-304">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="cd5f6-305">Из командлета `Get-AzSqlServerServiceObjective` удален нерекомендуемый параметр `DatabaseName`</span><span class="sxs-lookup"><span data-stu-id="cd5f6-305">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="cd5f6-306">Из командлета `Set-AzSqlDatabaseDataMaskingPolicy` удален нерекомендуемый параметр `PrivilegedLogin`</span><span class="sxs-lookup"><span data-stu-id="cd5f6-306">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="cd5f6-307">Az.Storage (ранее Azure.Storage и AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-307">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="cd5f6-308">Для поддержки создания контекста хранения Oauth только с именем учетной записи хранения набор параметров по умолчанию был изменен на `OAuthParameterSet`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-308">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="cd5f6-309">Например, `$ctx = New-AzureStorageContext -StorageAccountName $accountName`.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-309">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="cd5f6-310">Параметр `Location` стал обязательным в командлете `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="cd5f6-310">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="cd5f6-311">Методы API службы хранилища теперь используют асинхронную модель на основе задач (TAP) вместо синхронных вызовов API.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-311">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="cd5f6-312">В приведенных ниже примерах показаны новые асинхронные команды.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-312">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="cd5f6-313">Моментальный снимок большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="cd5f6-313">Blob Snapshot</span></span>

<span data-ttu-id="cd5f6-314">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-314">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="cd5f6-315">Az:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-315">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="cd5f6-316">Общий доступ к снимку</span><span class="sxs-lookup"><span data-stu-id="cd5f6-316">Share Snapshot</span></span>

<span data-ttu-id="cd5f6-317">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-317">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="cd5f6-318">Az:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-318">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="cd5f6-319">Отмена удаления обратимо удаленных больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="cd5f6-319">Undelete soft-deleted blob</span></span>

<span data-ttu-id="cd5f6-320">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-320">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="cd5f6-321">Az:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-321">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="cd5f6-322">Установка уровня большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="cd5f6-322">Set Blob Tier</span></span>

<span data-ttu-id="cd5f6-323">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-323">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="cd5f6-324">Az:</span><span class="sxs-lookup"><span data-stu-id="cd5f6-324">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="cd5f6-325">Az.Websites (ранее AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="cd5f6-325">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="cd5f6-326">Из объектов `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` и `PSSite` удалены нерекомендуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="cd5f6-326">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
